<script>
export default {
	name: 'mainTheme',
	data() {
		return {
			titles: [
				{ id: 1, title: '123', subtitle: '123' },
				{ id: 2, title: '123', subtitle: '123' },
				{ id: 3, title: '123', subtitle: '123' },
				{ id: 4, title: '123', subtitle: '123' }
			]
		}
	}
}
</script>

<template>
	<div>
		<div class="themes__bg" />
		<div class="wrapper">
			<div class="horizontal-line"></div>
			<div class="red-rectangle"></div>
			<h3>ТЕМЫ</h3>
			<div class="container">
				<div class="item item_1">
					<div class="title">
						<h2 class="theme__title">СПОРТ</h2>
						<img src="../../assets/arrow 2.svg" alt='arrow' />
					</div>
					<img src="../../assets/rapper.png" alt="Фотография статьи" />
					<p class="item_2-subtitle">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
				</div>
				<div class="item item_2">
					<div class="title">
						<h2 class="theme__title">ТУРИЗМ</h2>
						<img src="../../assets/arrow 2.svg" alt='arrow' />
					</div>
					<img src="../../assets/brige.png" alt="Фотография статьи" />
					<p class="item_2-subtitle">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
				</div>
				<div class="item item_3">
					<div class="title">
						<h2 class="theme__title">ПАРТНЕРЫ</h2>
						<img src="../../assets/arrow 2.svg" alt='arrow' />
					</div>
					<img src="../../assets/islam.png" alt="Фотография статьи" />
					<p class="item_2-subtitle">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
				</div>
				<div class="item item_4">
					<div class="title">
						<h2 class="theme__title">ПРОЕКТЫ</h2>
						<img src="../../assets/arrow 2.svg" alt='arrow' />
					</div>
					<img src="../../assets/september11.png" alt="Фотография статьи" />
					<p class="item_2-subtitle">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="border"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
.wrapper {
	max-width: 1480px;
	margin: 0 auto;
	padding: 0 20px;
}
.container {
	margin: 0 auto;
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: auto;
	gap: 20px;
	padding-bottom: 100px;
	justify-content: center;
}
.item {
	max-width: 340px;
}
.border {
	max-width: 340px;
	height: 0px;
	color: #aaaaaa;
	margin: 10px 0;
}

.themes__bg {
	width: 100%;
	height: 310px;
	background-color: black;
	position: absolute;
	z-index: -1;
	margin-top: -40px;
}

.theme__title {
	margin-top: 0;
	font-weight: bold;
	font-size: 32px;
	color: white;
}
.title {
	display: flex;
	flex-direction: row;
	gap:20px;
}

h3 {
	margin: 16px 0 32px 5px;
	font-size: 36px;
	font-weight: bold;
	color: white;
}

.horizontal-line {
	height: 0.3px;
	opacity: 1;
	width: 100%;
	border-top: 1px solid;
	margin: 0 auto;
}

.red-rectangle {
	width: 88px; /* ширина прямоугольника */
	height: 8px; /* высота прямоугольника */
	background-color: #aa0000; /* цвет фона прямоугольника */
	margin-bottom: 10px;
}
.diviver {
	height: 1px;
	width: 90%;
	margin-left: 5px;
	background-color: black;
}
.item_2-subtitle {
	font-family: 'Roboto Condensed';
	margin: 16px 0;
	font-size: 20px;
	font-weight: 700;
}
.item_2-list {
	font-size: 16px;
}

@media screen and (width < 769px) {
	.wrapper {
		margin-bottom: 20px;
		padding: 10px 20px 5px 20px;
		width: 100%;
	}
	.container {
		padding: 10px;
		width: 100%;
		grid-template-columns: repeat(4, 100vw);
		grid-template-rows: auto;
		scroll-snap-type: x mandatory;
		overflow-x: scroll;
		gap: 0px;
		justify-content: flex-start;
	}
	.item {
		display: flex;
		flex-direction: column;
		max-width: 90%;
		padding-left: 20px;
		padding-right: 20px;
		scroll-snap-align: start;
	}
	
	.theme__title {
		font-size: 20px;
	}
	h3 {
		font-family: "Roboto Condensed";
		text-transform: uppercase;
		font-size: 24px;
		font-weight: 400;
		line-height: 150%;
		margin: 6px 0 16px;
	}
	p {
		font-size: 16px;
	}
	.item_2-subtitle,
	.item_2-list,
	.img {
		width: 100%;
	}
}
</style>
