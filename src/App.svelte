<script>
	let appetizer = true
	let banhMi = true
	const toggleAppetizer = () => {
		appetizer = !appetizer
	}
	const toggleBanhMi = () => {
		banhMi = !banhMi
	}
</script>

<main>
	<header class="bg-black py-5">
		<h1 class="text-white TITLE">PHỞ HÀ NỘI</h1>
		<h4 class="text-white">(352) 373-2098</h4>
		<h4 class="text-white">3550 SW 34th Street</h4>
		<h4 class="text-white">Dine In or Carry Out from 11:00AM - 9:30PM</h4>
	</header>
	<div class="p-3 menu">
		<h1 class="p-4">Menu</h1>
		
		<h2 class="mc-title p-1 pb-2" on:click={toggleAppetizer}>Appetizers</h2>
		{#if appetizer == true}
			<hr>
			<div class="menu-category">
				<div class="menu-item">
					<h3>A-1 CHẢ GIÒ (2)</h3>
					<span>Crispy fried Vietnamese egg rolls. Served with Fish Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-2 CHẢ HŨ CHAY (2)</h3>
					<span>Crispy fried vegetarian egg rolls. Served with Pineapple Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-3 GỎI CUỐN (2)</h3>
					<span>Vietnamese Soft Spring Rolls - Choice of Shrimp and Pork, Tofu, Grilled Pork or Chicken, Vermicelli Noodles, Lettuce and Cilantro wrapped in clear rice paper. Served with Peanut Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-4 Edamame</h3>
					<span>Boiled Green Soybeans finished with a light dusting of Sea Salt. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-5 Dumplings</h3>
					<span>Choice of Pan Fried or Steamed Chicken Dumplings served with Ginger Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-6 Mực Chiên Giòn</h3>
					<span>Crispy Fried Squid served with Vietnamese Pineapple Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-7 Spinach Soup</h3>
					<span>Spinach Soup Spinach and Tofu in a savory Chicken Broth. $3.5</span>
				</div>
				<div class="menu-item">
					<h3>A-8 Mushroom Soup</h3>
					<span>Mushroom and Tofu in a Savory Chicken Broth. $3.5</span>
				</div>
				<div class="menu-item">
					<h3>A-9 Shrimp Cake (4)</h3>
					<span>Battered Sweet Potato Fries topped with Shrimp and served with Vietnamese Fish Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-10 Samosas (4)</h3>
					<span>Chicken marinated with Yellow Curry deep-fried in Wonton Skins and served with Pineapple Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-11 Butterfly Shrimp</h3>
					<span>Shrimp Breaded and Fried. Served with Pineapple Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-12 CRISPY FRIED CHICKEN WINGS (8)</h3>
					<span>Crispy fried chicken wings tossed in choice of Sweet Chili or Vietnamese Fish Sauce. $11</span>
				</div>
			</div>
		{/if}
		<h2 class="mc-title p-1 pb-2" on:click={toggleBanhMi}>Bánh Mì - Vietnamese Sandwiches</h2>
		{#if banhMi == true}
			<hr>
			<div class="menu-category">
				<div class="menu-item">
					<h3>A-1 CHẢ GIÒ (2)</h3>
					<span>Crispy fried Vietnamese egg rolls. Served with Fish Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-2 CHẢ HŨ CHAY (2)</h3>
					<span>Crispy fried vegetarian egg rolls. Served with Pineapple Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-3 GỎI CUỐN (2)</h3>
					<span>Vietnamese Soft Spring Rolls - Choice of Shrimp and Pork, Tofu, Grilled Pork or Chicken, Vermicelli Noodles, Lettuce and Cilantro wrapped in clear rice paper. Served with Peanut Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-4 Edamame</h3>
					<span>Boiled Green Soybeans finished with a light dusting of Sea Salt. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-5 Dumplings</h3>
					<span>Choice of Pan Fried or Steamed Chicken Dumplings served with Ginger Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-6 Mực Chiên Giòn</h3>
					<span>Crispy Fried Squid served with Vietnamese Pineapple Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-7 Spinach Soup</h3>
					<span>Spinach Soup Spinach and Tofu in a savory Chicken Broth. $3.5</span>
				</div>
				<div class="menu-item">
					<h3>A-8 Mushroom Soup</h3>
					<span>Mushroom and Tofu in a Savory Chicken Broth. $3.5</span>
				</div>
				<div class="menu-item">
					<h3>A-9 Shrimp Cake (4)</h3>
					<span>Battered Sweet Potato Fries topped with Shrimp and served with Vietnamese Fish Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-10 Samosas (4)</h3>
					<span>Chicken marinated with Yellow Curry deep-fried in Wonton Skins and served with Pineapple Sauce. $4</span>
				</div>
				<div class="menu-item">
					<h3>A-11 Butterfly Shrimp</h3>
					<span>Shrimp Breaded and Fried. Served with Pineapple Sauce. $7</span>
				</div>
				<div class="menu-item">
					<h3>A-12 CRISPY FRIED CHICKEN WINGS (8)</h3>
					<span>Crispy fried chicken wings tossed in choice of Sweet Chili or Vietnamese Fish Sauce. $11</span>
				</div>
			</div>
		{/if}
	</div>
</main>

<style>
	@font-face{
		font-family: titleFont;
		src: url(../fonts/Barlow_Semi_Condensed/BarlowSemiCondensed-Light.ttf)
	}

	main {
		
		text-align: center;
		max-width: 240px;
		margin: 0 auto;
	}

	header {
		font-family: titleFont;
		background: black;
	}

	h1 {
		text-transform: uppercase;
		font-size: 5em;
		font-weight: 100;
	}

	h2{
		font-size: 2.5em;
	}

	h3{
		padding-top: 1em;
	}

	.menu {
		font-family: titleFont;
		background: #E2F3FF;
	}

	.mc-title:hover {
		background: rgba(0, 0, 0, .05);
		transition: .3s all;
	}

	.menu-category {
		display: flex;
		justify-content: center;
		flex-direction: row;
		flex-flow: wrap;
	}

	.menu-item {
		width: 400px;
		margin: .5em;
		padding: 6px;
		height: auto;
		text-align: center;
		border: 1px all black;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>