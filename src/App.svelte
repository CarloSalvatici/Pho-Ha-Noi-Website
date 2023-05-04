<script>
	import axios from "axios"
	import { onMount } from 'svelte'
	import menuData from "../public/menuData.json";
	$: innerWidth = 0
	const url = 'https://carlo-web.herokuapp.com/api/accounts'
	let displayCategories = false
	let displayedCategory = "0"

	onMount(async () => {
		try {
			let res = await axios.get(url, {params: {getType: "getBusinessDataOf", businessName: "whatever"}})
			console.log(res.data.msg)
		} catch(err) {
			console.log(err)
		}
	})

	const mcToggle = () => {
		displayCategories = !displayCategories
	}

	const changeCategory = (index) => {
		displayedCategory = index
		displayCategories = false
	}

	const testFunction = (data) => {
		console.log(data)
	}

</script>

<svelte:window bind:innerWidth />

<main>
	<header class="bg-black py-5">
		<div class="title my-2 mb-4">
			<h1 class="text-white title-text my-0 me-3">PHỞ HÀ NỘI</h1>
			<img class="pho-bowl-image" src="pho-bowl.png" alt="Pho Bowl">
		</div>
		<h4 class="text-white phone-number"><a href="tel:3523732098">(352) 373-2098</a></h4>
		<address>
			<h4 class="text-white"><a target="_blank" and rel="noopener noreferrer" href="https://goo.gl/maps/6JiTCHbQfNDFv6gVA">3550 SW 34th Street, Gainesville FL</a></h4>
		</address>
		<h4 class="text-white">Dine In or Carry Out from 11:00AM - 9:30PM</h4>
	</header>
	<div class="p-3 menu">
		<h1 class="p-4 menu-title">Menu</h1>
		<div class="menu-not-the-part-that-says-menu">
			<div class="menu-category-titles">
				{#if innerWidth < 700}
				<button class="mc-toggle py-1 px-3" on:click={mcToggle}>
					<h2 class="mt-2">
						{#if displayCategories == true}Collapse Categories <img class="mc-expand" src="expand-arrow-up.png" alt="Expand Arrow">{/if}
						{#if displayCategories == false}View Categories <img class="mc-expand" src="expand-arrow-down.png" alt="Expand Arrow">{/if}
					</h2>
				</button>
				{/if}
				{#if displayCategories == true || innerWidth > 699}
					{#each menuData as data}
						<button class="mc-title p-1 pb-2 mt-1 {displayedCategory === menuData.indexOf(data) ? 'selected' : ''}" on:click={() => changeCategory(menuData.indexOf(data))}>
							<h2 class="mb-0">{data.categoryTitle}</h2>
						</button>
					{/each}
				{/if}
			</div>
			<div class="menu-category-contents">
				{#if innerWidth < 701}
					<h2 class="mc-mobile-title pt-4 mb-0">{menuData[displayedCategory].categoryTitle}</h2>
				{/if}
				{#if menuData[displayedCategory].description != undefined && menuData[displayedCategory].description != ""}
					<span>{menuData[displayedCategory].description}</span>
					<hr>
				{/if}
				<div class="mc-item-list">
					{#each menuData[displayedCategory].items as data}
							<div class="mc-item">
								<h3>{data.name}</h3>
								<span>{data.description} {data.price}</span>
							</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</main>

<style>
	@font-face{
		font-family: titleFont;
		src: url(../fonts/Barlow_Semi_Condensed/BarlowSemiCondensed-Light.ttf)
	}

	main {
		text-align: center;
		margin: 0 auto;
	}

	header {
		font-family: titleFont;
		background: black;
		width: 100%;
	}

	h1 {
		text-transform: uppercase;
		font-size: 5em;
		font-weight: 100;
	}

	h2 {
		font-size: 2em;
	}

	h3{
		padding-top: 1em;
	}

	h4 > a {
		text-decoration: none;
		color: white;
		transition: all .3s;
	}

	h4 > a:hover{
		color: rgb(210,210,210);
	}

	header > address {
		margin: auto;
	}

	.title-text {
		display: inline-block;
		vertical-align: middle;
	}

	.pho-bowl-image {
		display: inline-block;
		width: 110px;
		height: auto;
		vertical-align: middle;
	}

	.menu {
		text-align: center;
		margin: 0 auto;
		font-family: titleFont;
		background: #E2F3FF;
	}

	 /*menu takes up not the whole screen on larger window*/
	@media (max-width: 1649px) {
		.menu {
			max-width: 100%
		}
	}

	@media (min-width: 1650px) {
		.menu {
			max-width: 80%
		}	
	}

	.menu-category span{
		padding-top: 5px;
	}

	.menu-not-the-part-that-says-menu {
		display: flex;
	}


	@media (max-width: 1499px){
		.menu-category-titles {
			min-width: 40%;
			max-width: 40%;
		}
	}

	@media (min-width: 1500px) {
		.menu-category-titles {
			min-width: 500px;
			max-width: 500px;
		}
	}

	.menu-category-contents {
		flex-grow: 1;
	}



	.menu-title {
		border-bottom: 1px solid grey;
		padding: 0px 0px 20px 0px !important;
		margin-bottom: 15px;
	}

	.mc-toggle:hover {
		background: rgba(0, 100, 255, .05);
		transition: .3s all;
		cursor: pointer;
	}

	.mc-toggle {
		border: 2px black solid;
		width: fit-content;
		margin: auto;
	}

	.mc-expand {
		width: 23px;
		position: relative;
		transform: translateY(-5%);
	}

	.mc-title {
		display: inline-block;
		border: 1px #e2f3ff solid;
		background: none;
		transition: .3s all;
		width: 100%;
	}

	.mc-title:nth-child(odd) {
		background: rgb(215, 236, 255) !important;
	}

	.selected {
		border: 1px black solid;
	}

	.mc-title:hover {
		background: rgba(0, 100, 255, .05);
		transition: .3s all;
		cursor: pointer;
	}

	.mc-item-list {
		display: flex;
		justify-content: center;
		flex-direction: row;
		flex-flow: wrap;
		padding-bottom: 1em;
	}

	.mc-item {
		margin: .3em;
		padding: 6px;
		height: auto;
		text-align: center;
		border: 1px all black;
	}

	@media (min-width: 1398px) {
		.mc-item{
			width: 400px;
		}
	}
	@media (max-width: 1397px) {
		.mc-item{
			width: 100%;
		}
	}

	@media (min-width: 800px) {
		main {
			max-width: none;
		}
	}

	@media (max-width: 699px) {
		.menu-not-the-part-that-says-menu {
			display: block;
		}
		.menu-category-titles {
			margin: auto;
			min-width: 100%;
			max-width: 100%;
		}
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>