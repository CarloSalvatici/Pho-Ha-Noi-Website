<script>

	$: innerWidth = 0

	let displayCategories = false
	const mcToggle = () => {
		displayCategories = !displayCategories
	}

	let displayedCategory = "appetizer"
	const toggleappetizer = () => {
		displayedCategory = "appetizer"
		displayCategories = false
	}
	const togglebanhMi = () => {
		displayedCategory = "banhMi"
		displayCategories = false
	}
	const togglegoi = () => {
		displayedCategory = "goi"
		displayCategories = false
	}
	const togglefriedRice = () => {
		displayedCategory = "friedRice"
		displayCategories = false
	}
	const togglespecial = () => {
        displayedCategory = "special"
		displayCategories = false
	}
	const togglepho = () => {
        displayedCategory = "pho"
		displayCategories = false
	}
	const toggleporkSoup = () => {
        displayedCategory = "porkSoup"
		displayCategories = false
	}
	const togglericePlatter = () => {
        displayedCategory = "ricePlatter"
		displayCategories = false
	}
	const togglevermicelli = () => {
        displayedCategory = "vermicelli"
		displayCategories = false
	}
	const togglevegetarian = () => {
        displayedCategory = "vegetarian"
		displayCategories = false
	}
	const togglefish = () => {
        displayedCategory = "fish"
		displayCategories = false
	}
	const togglesquid = () => {
        displayedCategory = "squid"
		displayCategories = false
	}
	const toggleshrimp = () => {
        displayedCategory = "shrimp"
		displayCategories = false
	}
	const togglespecialties = () => {
        displayedCategory = "specialties"
		displayCategories = false
	}
	const toggledessert = () => {
        displayedCategory = "dessert"
		displayCategories = false
	}
	const togglesides = () => {
        displayedCategory = "sides"
		displayCategories = false
	}
	const toggledrinks = () => {
        displayedCategory = "drinks"
		displayCategories = false
	}
</script>

<svelte:window bind:innerWidth />

<main>
	<header class="bg-black py-5">
		<div class="title my-2 mb-4">
			<h1 class="text-white title-text my-0 me-3">PHỞ HÀ NỘI</h1>
			<img class="pho-bowl-image" src="pho-bowl.png" alt="Pho Bowl">
		</div>
		<h4 class="text-white">(352) 373-2098</h4>
		<h4 class="text-white">3550 SW 34th Street</h4>
		<h4 class="text-white">Dine In or Carry Out from 11:00AM - 9:30PM</h4>
	</header>
	<div class="p-3 menu">
		<h1 class="p-4 menu-title">Menu</h1>
		<div class="menu-not-the-part-that-says-menu">
			<div class="menu-category-titles">
				{#if innerWidth < 700}
				<h2 class="mc-toggle pt-1 pb-2 px-3 my-1" on:click={mcToggle}>{#if displayCategories == true}Collapse Categories <img class="mc-expand" src="expand-arrow-up.png" alt="Expand Arrow">{/if}
				{#if displayCategories == false}View Categories <img class="mc-expand" src="expand-arrow-down.png" alt="Expand Arrow">{/if}</h2>
				{/if}
				{#if displayCategories == true || innerWidth > 699}
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='appetizer' ? 'selected' : ''}" on:click={toggleappetizer}>Appetizers</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='banhMi' ? 'selected' : ''}" on:click={togglebanhMi}>Bánh Mì - Vietnamese Sandwiches</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='goi' ? 'selected' : ''}" on:click={togglegoi}>Gỏi - Vietnamese Salad</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='friedRice' ? 'selected' : ''}" on:click={togglefriedRice}>Cơm Chiên - Fried Rice</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='special' ? 'selected' : ''}" on:click={togglespecial}>Special</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='pho' ? 'selected' : ''}" on:click={togglepho}>Phở</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='porkSoup' ? 'selected' : ''}" on:click={toggleporkSoup}>Hủ Tiếu - Noodle Soup in Pork Broth</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='ricePlatter' ? 'selected' : ''}" on:click={togglericePlatter}>Cơm Dĩa - Rice Platter</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='vermicelli' ? 'selected' : ''}" on:click={togglevermicelli}>Bún - Rice Vermicelli</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='vegetarian' ? 'selected' : ''}" on:click={togglevegetarian}>Dĩa Chay - Vegetarian Dishes</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='fish' ? 'selected' : ''}" on:click={togglefish}>Cả - Fish</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='squid' ? 'selected' : ''}" on:click={togglesquid}>Mực - Squid</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='shrimp' ? 'selected' : ''}" on:click={toggleshrimp}>Tôm - Shrimp</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='specialties' ? 'selected' : ''}" on:click={togglespecialties}>Hà Nội Specialties</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='dessert' ? 'selected' : ''}" on:click={toggledessert}>Dessert</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='sides' ? 'selected' : ''}" on:click={togglesides}>Sides and Extra</h2>
					<h2 class="mc-title p-1 pb-2 my-1 {displayedCategory ==='drinks' ? 'selected' : ''}" on:click={toggledrinks}>Drinks</h2>
				{/if}
			</div>
			<div class="menu-category-contents">
				{#if displayedCategory == "appetizer"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Appetizers</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>A-1 Chả Giò (2)</h3>
								<span>Crispy fried Vietnamese egg rolls. Served with Fish Sauce. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-2 Chả Giò Chay (2)</h3>
								<span>Crispy fried vegetarian egg rolls. Served with Pineapple Sauce. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-3 Gỏi Cuốn (2)</h3>
								<span>Vietnamese Soft Spring Rolls - Choice of Shrimp and Pork, Tofu, Grilled Pork or Chicken, Vermicelli Noodles, Lettuce and Cilantro wrapped in clear rice paper. Served with Peanut Sauce. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-4 Edamame</h3>
								<span>Boiled Green Soybeans finished with a light dusting of Sea Salt. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-5 Dumplings</h3>
								<span>Choice of Pan Fried or Steamed Chicken Dumplings served with Ginger Sauce. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-6 Mực Chiên Giòn</h3>
								<span>Crispy Fried Squid served with Vietnamese Pineapple Sauce. $7.5</span>
							</div>
							<div class="mc-item">
								<h3>A-7 Spinach Soup</h3>
								<span>Spinach Soup Spinach and Tofu in a savory Chicken Broth. $4</span>
							</div>
							<div class="mc-item">
								<h3>A-8 Mushroom Soup</h3>
								<span>Mushroom and Tofu in a Savory Chicken Broth. $4</span>
							</div>
							<div class="mc-item">
								<h3>A-10 Samosas (4)</h3>
								<span>Chicken marinated with Yellow Curry deep-fried in Wonton Skins and served with Pineapple Sauce. $4.5</span>
							</div>
							<div class="mc-item">
								<h3>A-11 Butterfly Shrimp</h3>
								<span>Shrimp Breaded and Fried. Served with Pineapple Sauce. $7.5</span>
							</div>
							<div class="mc-item">
								<h3>A-12 Crispy Fried Chicken Wings (8)</h3>
								<span>Crispy fried chicken wings tossed in choice of Sweet Chili or Vietnamese Fish Sauce. $12</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "banhMi"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Bánh Mì - Vietnamese Sandwiches</h2>
						{/if}
						<span>A light, crisp authentic bite of Vietnam, served on toasted French baguette with our homemade paté and mayonnaise, pickled carrots and daikon, cucumber, fresh jalapeños, cilantro, salt, pepper, and soy sauce.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>#1 Bẩnh Mì Đặc Biệt - Combination</h3>
								<span>Sliced French ham (jambon), pork, cured pork roll and paté. $7</span>
							</div>
							<div class="mc-item">
								<h3>#2 Bẩnh Mì Thịt - Sliced Pork</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#3 Bẩng Mì Chả - Sliced Cured Pork Roll</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#4 Bẩnh Mì Thịt Gà Nướng - Grilled Pork</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#5 Bẩnh Mì Thịt Heo Nướng</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#6 Bình Mì Xả Xìu </h3>
								<span>Slow roasted pork marinated in Chinese-style barbecue and finished with BBQ glaze. $6.5</span>
							</div>
							<div class="mc-item">
								<h3>#7 Bánh Mì Chả & Thịt - Sliced Cured Pork Roll And Pork</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#8 Bánh Mì Bì - Shredded Pork Skins</h3>
								<span>Crunchy, textured strands of pork skin tossed with onions in Vietnamese Fish Sauce. $6.5</span>
							</div>
							<div class="mc-item">
								<h3>#9 Bình Mì Bò Xào - Sliced Stir Fried Beef</h3>
								<span>Sliced beef and onions marinated in house seasonings. $6.5</span>
							</div>
							<div class="mc-item">
								<h3>#10 Bình Mì Chả & Paté - Sliced Cured Pork Roll And Paté</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#11 Bánh Mì Paté - Paté Spread</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#12 Bánh Mì Ham & Giả - Jambon And Sliced Cured Pork Roll</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#13 Bánh Mì Ham Paté - Jambon And Paté Spread</h3>
								<span>$6.5</span>
							</div>
							<div class="mc-item">
								<h3>#14 Bánh Mì Chay - Vegetarian</h3>
								<span>Tofu and mixed vegetables wok fried in house seasonings. $6.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "goi"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Gỏi - Vietnamese Salad</h2>
						{/if}
						<span>A deliciously fresh and vibrant salad composed of shredded purple cabbage and green cabbage, onions, pickled carrots and daikon, topped with cilantro, roasted onions and peanuts. All served with Vietnamese Fish Sauce and crispy shrimp chips on the side.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>G-1 Gỏi Tôm</h3>
								<span>Shrimp Salad $9.5</span>
							</div>
							<div class="mc-item">
								<h3>G-2 Gỏi Gà</h3>
								<span>Chicken Salad $8.5</span>
							</div>
							<div class="mc-item">
								<h3>G-3 Gỏi Chay</h3>
								<span>Vegetarian Tofu Salad $7.5</span>
							</div>
							<div class="mc-item">
								<h3>G-4 Gỏi Thập Cẩm</h3>
								<span>Combination Pork, Shrimp, and Chicken Salad $10.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "friedRice"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Cơm Chiên - Fried Rice</h2>
						{/if}
						<span>A light yet flavorful wok fried rice seasoned with soy sauce, fish sauce, salt, black pepper, and scrambled eggs. Accompanied by beansprouts and scallions upon request.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>F-1 Cơm Chiên Tôm</h3>
								<span>Shrimp Fried Rice. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>F-2 Cơm Chiên Gà</h3>
								<span>Chicken Fried Rice $13</span>
							</div>
							<div class="mc-item">
								<h3>F-3 Cơm Chiên Bộ</h3>
								<span>Beef Fried Rice $13</span>
							</div>
							<div class="mc-item">
								<h3>F-4 Cơm Chiên Thập Càm</h3>
								<span>Combination Fried Rice (Shrimp, Chicken, Beef) $13.5</span>
							</div>
							<div class="mc-item">
								<h3>F-5 Cơm Chiên Chay</h3>
								<span>Vegetable Fried Rice with Tofu $13</span>
							</div>
							<div class="mc-item">
								<h3>F-6 Cơm Chiên Xã Xìu</h3>
								<span>Barbeque Pork Fried Rice $13</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "special"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Special</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>SP-1 Vietnamese Curry Soup</h3>
								<span>A traditional bone-in chicken curry soup served with sweet potato, potato, and a side of white/yellow rice, vermicelli noodles or French bread. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SP-2 House Special Pork Fried Rice</h3>
								<span>A light and flavorful fried rice with BBQ pork, grilled pork, and mixed veggies. $13.5<span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "pho"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Phở</h2>
						{/if}
						<span>An aromatic and savory soup served with thin rice noodles over our signature beef broth with sliced onions, scallions, and cilantro. All soups come with a side of fresh beansprouts, jalapenos, lime, and Thai basil.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>P-1 Phở Hà Nội Xe Lữa</h3>
								<span>House special combination soup served with thin slices of medium rare beef, brisket, flank, tendon, tripe, and sliced beef meatballs. $15</span>
							</div>
							<div class="mc-item">
								<h3>P-2 Phở Tái, Nạm, Gân, Sảch</h3>
								<span>Rice noodle soup with thin slices of medium rare beef, flank, tendon, and tripe. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>P-3 Phở Tái Nạm</h3>
								<span>Rice noodle soup with thin slices of medium rare beef and flank. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-4 Phở Tái Gân</h3>
								<span>Rice noodle soup with thin slices of medium rare beef and tendon. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-5 Phở Tái Sảch</h3>
								<span>Rice noodle soup with thin slices of medium rare beef and tripe. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-6 Phở Tái</h3>
								<span>Rice noodle soup with thin slices of medium rare beef. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-7 Phở Bò Viên</h3>
								<span>Rice noodle soup with sliced meatballs. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-8 Phở Gà</h3>
								<span>Rice noodle soup serve with white chicken in a savory chicken broth. $13</span>
							</div>
							<div class="mc-item">
								<h3>P-9 Phở Chay</h3>
								<span>Rice noodle soup with mixed vegetables and tofu in a vegetarian broth. $13</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "porkSoup"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Hủ Tiếu - Noodle Soup in Pork Broth</h2>
						{/if}
						<span>Your choice of either rice noodle, egg noodles, or a combination of both served with or without our delicious, fragrant homemade pork broth and finished with fried shallots and chives. All soups come with a side of beansprouts, lime, jalapeños, and Thai basil.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>T-1 Hủ Tiếu Hà Nội</h3>
								<span>Noodle soup with BBQ pork and seafood medly of crab meat, squid, and shrimp. $15</span>
							</div>
							<div class="mc-item">
								<h3>T-2 Hủ Tiếu Xả Xíu</h3>
								<span>Noodle soup with our slow roasted Chinese BBQ pork. $13</span>
							</div>
							<div class="mc-item">
								<h3>T-3 Hủ Tiếu Tôm Chiên</h3>
								<span>Noodle soup with fried shrimp. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>T-4 Hủ Tiếu Bò Viên</h3>
								<span>Noodle soup with sliced meatballs. $13</span>
							</div>
							<div class="mc-item">
								<h3>T-5 Hủ Tiếu Hải Sản</h3>
								<span>Noodle soup with seafood combination of crab meat, squid, and shrimp. $15</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "ricePlatter"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Cơm Dĩa - Rice Platter</h2>
						{/if}
						<span>Rice entrees are served with your choice of white or yellow rice, a side of lettuce, tomato, pickled carrots and daikon, and a sweet and tangy Vietnamese Fish Sauce.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>#1 Cơm Thịt Heo Nướng</h3>
								<span>Rice with grilled pork. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#2 Cơm Bì Thịt Heo Nướng</h3>
								<span>Rice with grilled pork and shredded pork skins. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#3 Cơm Bì Chả Thịt Heo Nướng</h3>
								<span>Rice with shredded pork skins, steamed egg cake, and grilled pork. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>#4 Cơm Thịt Bì Xào Hành Tây</h3>
								<span>Rice with stir fried beef and onions. $13</span>
							</div>
							<div class="mc-item">
								<h3>#5 Cơm Thịt Bỏ Xào Rau Cải</h3>
								<span>Rice with stir fried beef and vegetables. $13</span>
							</div>
							<div class="mc-item">
								<h3>#6 Cơm Gà Hà Nội Xào Chua Ngọt</h3>
								<span>Breaded chicken, bamboo shoots, and mixed vegetables wok sautéed in a sweet and sour brown glaze. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#7 Cơm Gà Xào Lăn</h3>
								<span>Chicken and glass noodles with onions, celery, carrots, and diced blacked mushrooms in a yellow curry and fish sauce blend. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#8 Cơm Gà Xào Hạt Điều</h3>
								<span>White meat chicken stir fried with onions, celery, and green peppers in a cashew sauce. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#9 Cơm Gà Nướng</h3>
								<span>Rice with grilled chicken. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>#10 Cơm Gà Xào Rau Cải</h3>
								<span>Rice with stir fried chicken and mixed vegetables. $12.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "vermicelli"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Bún - Rice Vermicelli</h2>
						{/if}
						<span>A salad-style rice noodle bowl that starts with a base of shredded lettuce, cucumber, and beansprouts topped with rice vermicelli noodles finished with crunchy peanuts, and fried onion topping. Served with Vietnamese Fish Sauce on side.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>V-1 Bún Gà Nướng</h3>
								<span>Rice vermicelli with grilled chicken. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>V-2 Bún Heo Nướng</h3>
								<span>Rice vermicelli with grilled pork. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>V-3 Bún Chả Giò</h3>
								<span>Rice vermicelli with crispy egg rolls. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>V-4 Bún Chả Giò Thịt Nướng</h3>
								<span>Rice vermicelli with crispy egg rolls and choice of grilled pork or chicken. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>V-5 Bún Bỏ Xào</h3>
								<span>Rice vermicelli with stir fried lemongrass, beef, and onions. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>V-6 Bún Gà Xào</h3>
								<span>Rice vermicelli with stir fried lemongrass, chicken, and onions. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>V-7 Bún Chả Giò Chay</h3>
								<span>Rice vermicelli with vegetarian egg rolls and tofu. $12.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "vegetarian"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Dĩa Chay - Vegetarian Dishes</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>VG-1 Cơm Đậu Hủ Chiên Sốt Cà</h3>
								<span>White or yellow rice with fried tofu in tomato sauce. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>VG-2 Cơm Đầu Hủ Chiên Xào Rau</h3>
								<span>White or yellow rice with stir fried tofu and vegetables. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>VG-3 Bủn Rau Đậu Hủ</h3>
								<span>Rice vermicelli with steamed mixed vegetables and tofu. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>VG-4 Bủn Xào Rau Đậu Hủ</h3>
								<span>Rice vermicelli with stir fried tofu and mixed vegetables. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>VG-5 Mì Xào Dòn Hay Mềm Rau Cải</h3>
								<span>Pan fried egg noodles (soft or crispy) with vegetables. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>VG-6 Mì Xào Dòn Hay Mềm Rau Cài Đậu Hủ</h3>
								<span>Pan fried egg noodles (soft or crispy) with tofu and vegetables. $13</span>
							</div>
							<div class="mc-item">
								<h3>VG-7 Phở Xao Rau Cải Đấu Hú</h3>
								<span>Pan fried rice noodles with tofu and mixed vegetables. $13</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "fish"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Cả - Fish</h2>
						{/if}
						<span>Entrees include two whitefish fillets deep fried with a variety of different preparation and sauces. Served with white or yellow rice.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>FH-1 Cà Chiên Vàng Nước Mắm Gừng</h3>
								<span>Fried fish in ginger sauce. $14.45</span>
							</div>
							<div class="mc-item">
								<h3>FH-2 Cà Chiên Sốt Cà</h3>
								<span>Fried fish, tomatoes, and white onions in a tomato sauce. $14.45</span>
							</div>
							<div class="mc-item">
								<h3>FH-3 Cà Chiên Sốt Chua Ngọt</h3>
								<span>Fried fish, carrots, onions, bamboo shoots, celery, and water chestnuts wok sautéed in a sweet and sour sauce. $14.45</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "squid"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Mực - Squid</h2>
						{/if}
						<span>All squid entrees are served with white or yellow rice.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>SQ-1 Mực Xào Xã Ởt</h3>
								<span>Stir fried squid with lemongrass. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SQ-2 Mực Xào Chua Ngọt</h3>
								<span>Stir fried sweet and sour squid with mixed vegetables. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SQ-3 Mực Xào Cà Ri</h3>
								<span>Yellow curry squid stir fried with onions and green peppers. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SQ-4 Mực Xào Rau Cải</h3>
								<span>Stir fried squid with cucumber, celery, onions and tomatoes. $13.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "shrimp"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-2">Tôm - Shrimp</h2>
						{/if}
						<span>Shrimp entrees are served with white or yellow rice.</span>
						<hr>
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>SH-1 Tôm Rim</h3>
								<span>Shrimp marinated in pepper and fish sauce. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SH-2 Tôm Xào Xả Ớt</h3>
								<span>Shrimp with lemongrass stir-fry. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SH-3 Tôm Xào Cải Broccoli</h3>
								<span>Stir fried shrimp and broccoli. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SH-4 Tôm Xào Rau</h3>
								<span>Stir fried shrimp and mixed vegetables. $13.5</span>
							</div>
							<div class="mc-item">
								<h3>SH-5 Canh Chua Tôm</h3>
								<span>A tangy yet sweet hot-pot style shrimp soup with beansprouts, tomatoes, celery, and bamboo shoots in a lovely chicken broth base. $13.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "specialties"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Hà Nội Specialties</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>S-1 Bò Lúc Lắc - Vietnamese Shaken Beef</h3>
								<span>Chunks of tender beef sautéed with butter, garlic, and onions. Served with white or yellow rice, lettuce, tomato, and Vietnamese Fish Sauce. $14.95</span>
							</div>
							<div class="mc-item">
								<h3>S-2 Phở Áp Chảo Hà Nội - Wok Fried Rice Noodle</h3>
								<span>Pepper steak and mixed vegetables over wok fried rice noodles. $15.45</span>
							</div>
							<div class="mc-item">
								<h3>S-3 Mì Xào Dòn - Crispy Egg Noodles</h3>
								<span>A beautiful bird's nest formed from deep fried egg noodles, topped with your choice of stir fried beef, chicken, or BBQ Pork and mixed vegetables. $15.95</span>
							</div>
							<div class="mc-item">
								<h3>S-4 Bún Bò Huế - Spicy Beef Noodle Soup</h3>
								<span>A spicy combination of pork and beef broth with rice vermicelli noodles, sliced beef, pork, and pork roll. Garnished with sliced onions and lemongrass. Served with a side of beansprouts, limes, jalapeños, and Thai basil. $13</span>
							</div>
							<div class="mc-item">
								<h3>S-5 Bò Kho - Vietnamese Beef Stew</h3>
								<span>A traditional slow cooked beef stew with carrots accompanied by your choice of egg noodles, rice noodle, or French bread. $13</span>
							</div>
							<div class="mc-item">
								<h3>S-6 Thai Chicken Curry</h3>
								<span>White meat chicken, bamboo shoots, onions, carrots, celery, and water chestnuts in a coconut milk yellow curry sauce with your choice of white or yellow rice. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>S-7 Singapore Noodles</h3>
								<span>Glass noodles and mixed vegetables stir fried with beef or chicken in brown sauce. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>S-8 Bánh Xèo - Vietnamese Crepes</h3>
								<span>Two Vietnamese crepe pancakes, prepared in cast iron skillet with shrimp, chicken, pork and beansprouts. Served with large leaf lettuce, and House Vietnamese Fish Sauce. $13</span>
							</div>
							<div class="mc-item">
								<h3>S-10 Mongolian Beef</h3>
								<span>Sliced beef prepared Mongolian-style with onions and crispy white noodles, Served with white or yellow rice. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>S-11 Potato Curry</h3>
								<span>Choice of beef, chicken, or tofu cooked in a coconut milk yellow curry sauce with potatoes, onions, carrots, and celery. Served with white or yellow rice. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>S-12 Bách Thái</h3>
								<span>Rice noodle stir fry with tofu and mixed vegetables. Topped with chopped peanuts, cilantro, and lime wedges. $12.5</span>
							</div>
							<div class="mc-item">
								<h3>S-13 Bánh Canh - Tapioca Noodle Soup</h3>
								<span>An earthy comfort soup served with thick tapioca noodles, shrimp, pork, and BBQ pork in a combination of our savory chicken and pork broth and topped with green onions, fried shallots, and cilantro. Served with a side of fresh beansprouts, lime, jalapeños, and Thai basil. $13.5</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "dessert"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Dessert</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>D-1 Fried Bananas (6)</h3>
								<span>Sliced sweet banana deep fried in tempura batter and dusted in powdered sugar. $3</span>
							</div>
						</div>
					</div>
				{/if}
				{#if displayedCategory == "sides"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Sides and Extra</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>Side Steamed Rice</h3>
								<span>White or yellow. $1.5</span>
							</div>
							<div class="mc-item">
								<h3>Side Broth</h3>
								<span>Small $1.5, Medium $4, Large $6.5</span>
							</div>
							<div class="mc-item">
								<h3>Side Noodles</h3>
								<span>Rice Noodle $1.5, Egg Noodle $2</span>
							</div>
							<div class="mc-item">
								<h3>Steam Mixed Vegetables</h3>
								<span>$1.5</span>
							</div>
							<div class="mc-item">
								<h3>Extra Tofu</h3>
								<span>$1.5</span>
							</div>
							<div class="mc-item">
								<h3>Fried Egg</h3>
								<span>$1.25</span>
							</div>
							<div class="mc-item">
								<h3>Toasted French Baguette</h3>
								<span>$1.5</span>
							</div>
							<div class="mc-item">
								<h3>Extra Meat</h3>
								<span>Shrimp, chicken, pork, beef, BBQ pork, sliced cured pork, or meatballs. $3</span>
							</div>
						</div>
					</div>
				{/if}	
				{#if displayedCategory == "drinks"}
					<div class="menu-category">
						{#if innerWidth < 701}
							<h2 class="mc-mobile-title pt-4 mb-0">Drinks</h2>
						{/if}
						<div class="mc-item-list">
							<div class="mc-item">
								<h3>Vietnamese-Style French Coffee</h3>
								<span>$4.5</span>
							</div>
							<div class="mc-item">
								<h3>Fresh-Brewed Jasmine Blend Tea</h3>
								<span>Sweet or Unsweet, Hot or Cold $3.5</span>
							</div>
							<div class="mc-item">
								<h3>Domestic Beers</h3>
								<span>Budlight, Budweiser, Yuengling (Black and Tn, Traditional, and Light), First Magnitude 72 Pale Ale $4</span>
							</div>
							<div class="mc-item">
								<h3>Import Beers</h3>
								<span>Asahi, Kirin Light, Kirin Ichiban $5</span>
							</div>
							<div class="mc-item">
								<h3>Fountain Drink</h3>
								<span>Coke, Diet Coke, and Sprite $3</span>
							</div>
						</div>
					</div>
				{/if}
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

	.mc-title:nth-child(odd) {
		background: rgb(215, 236, 255);
	}

	.mc-title {
		display: block;
		border: 1px #e2f3ff solid;
	}

	.selected {
		border: 1px black solid;
	}

	.mc-title:hover {
		background: rgba(0, 100, 255, .05);
		transition: .3s all;
		cursor: pointer;
	}

	.mc-title {
		transition: .3s all;
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