<template>
	<div class="main">
		<div class="banner">
			<h1 class="banner__heading">Восточная Европа</h1>
		</div>
		<div class="list">
			<div class="wrapper">
				<div class="list__top top">
					<span class="top__line-red line-red"></span>
					<p class="top__text text-heading">ЦЕНТР ВОСТОЧНОЙ ЕВРОПЫ</p>
					
					<p class="bottom__text text-heading">Страны</p>
					
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CentralAsia'
}
</script>

<style scoped>
.container__card {
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-template-rows: repeat(4, 225px);
	grid-column-gap: 90px;
	grid-row-gap: 60px;
}

.item {
	display: flex;
	width: 650px;
}

.item__card {
	display: flex;
	justify-content: space-between;
	flex-direction: column;
}

.card__img {
	margin-right: 24px;
	width: 337px;
	height: 225px;
}

.main {
	flex-direction: column;
	margin: 0;
}

.wrapper {
	max-width: 1440px;
	margin: 0 auto;
}

.border__img {
	border: #979696 1px solid;
}

/* banner */
.banner {
	background-image: url('@/assets/shapka.png');
	background-repeat: no-repeat;
	background-size: 100% 100%;
	min-height: 340px;
	display: flex;
	justify-content: center;
	align-items: center;
}

.banner__heading {
	font-size: 80px;
	font-weight: bold;
	color: #ffffff;
}

/* list */
.list {
	margin-top: 10px;
}

.list__top {
	border-top: 1px solid #aaaaaa;
}

.line-red {
	display: block;
	height: 13px;
	width: 80px;
	background-color: #aa0000;
}

.text-heading {
	margin-bottom: 30px;
	margin-top: 24px;
	font-size: 36px;
	font-family: 'Roboto Condensed', sans-serif;
	text-transform: uppercase;
}

.card__img__top {
	width: 375px;
	height: 250px;
}

.list__bottom {
	border-top: 1px solid #aaaaaa;
	margin-top: 80px;
}

.bottom__list-cards {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
}

/* card */
.card {
	display: flex;
	margin-top: 32px;
}

.card__box {
	display: flex;
	flex-direction: column;
	margin-left: 24px;
	justify-content: space-between;
}

.card__heading {
	margin-bottom: 87px;
	font-size: 36px;
	font-family: 'Roboto Condensed', sans-serif;
}

.card__heading__item {
	margin-bottom: 20px;
}

.card__text {
	font-size: 20px;
	font-family: Roboto, sans-serif;
	margin-bottom: 4px;
}

.bottom {
	margin-bottom: 80px;
}

/* //////////////////// */

/* media request */

@media screen and (width < 1400px) {
	.bottom__list-cards {
		justify-content: center;
	}

	.top__card {
		justify-content: center;
	}

	.banner__heading {
		font-size: 60px;
	}
}

@media screen and (width < 1000px) {
	.banner__heading {
		font-size: 45px;
	}
}

@media screen and (width < 769px) {
	.main {
		padding: 10px;
	}

	.container__card {
		grid-column-gap: 0;
		grid-row-gap: 30px;
		display: flex;
		flex-direction: column;
	}

	.item {
		flex-direction: column;
	}

	.card {
		flex-direction: column;
	}

	.card__heading {
		margin-bottom: 0;
	}
}
</style>
