
<script>
import axios from 'axios'

export default {
	name: 'mainPolitic',
	data() {
		return {
			newsItems: [],
			apiUrlNews: 'http://localhost:5000/api/data_news_politics' // URL API для новостей политики
		}
	},
	mounted() {
		this.fetchNewsItems()
	},
	methods: {
		async fetchNewsItems() {
			try {
				const response = await axios.get(this.apiUrlNews)
				this.newsItems = response.data // Предполагается, что API возвращает массив новостей
			} catch (e) {
				console.error('Error fetching news items:', e)
			}
		}
	}
}

</script>

<template>
	<div class="wrapper">
		<div class="horizontal-line"></div>
		<div class="red-rectangle"></div>
		<h3>ПОЛИТИКА</h3>

		<div class="container">
			<div v-for="item in newsItems" :key="item.id" class="item">
				<img :src="item.url" alt="News image" />
				<p>{{ item.title }}</p>
			</div>
		</div>
	</div>
</template>

<style scoped>
.wrapper {
	max-width: 1480px;
	margin-bottom: 32px;
	padding: 0 20px 0 20px;
}

.container {
	margin: 0 auto;
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: 357px;
	gap: 20px;
}

h3 {
	font-weight: normal;
	font-size: 36px;
	margin: 6px 0px 16px 5px;
}

.horizontal-line {
	height: 0.3px;
	opacity: 0.4;
	width: 100%;
	background-color: #000;
	margin: 0 auto;
}

.red-rectangle {
	width: 88px;
	height: 8px;
	background-color: #aa0000;
	margin-bottom: 10px;
}

.item > p {
	font-family: 'Roboto Condensed';
	font-size: 20px;
	font-weight: bold;
	margin-top: 16px;
}

.item:nth-child(-n+1){
	display:none;
}


@media screen and (width < 769px) {
	.horizontal-line {
		width: 100%;
	}
	.wrapper {
		padding: 10px 20px 5px 20px;
		margin-bottom: 20px;
		width: 100%;
	}
	.container {
		padding: 10px;
		width: 100%;
		display: grid;
		grid-template-columns: 100vw 100vw 100vw;
		grid-template-rows: auto;
		scroll-snap-type: x mandatory;
		overflow-x: scroll;
	}
	h3 {
		margin: 6px 0 16px;
		font-family: "Roboto Condensed";
		text-transform: uppercase;
		font-size: 24px;
		font-weight: 400;
		line-height: 150%;
	}
	.item > p {
		font-size: 18px;
	}
	.item {
		display: none;
	}
	.item:nth-child(-n+3) {
		display: flex;
		flex-direction: column;
		width: 90%;
		padding-left: 20px;
		padding-right: 20px;
		scroll-snap-align: start;
	}
	
}
</style>
