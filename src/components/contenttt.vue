<template>
	<div style="padding-top: 10px;" class="main-col container">
		<div v-for="(image, index) in images" :key="index" class="col">
			<a :href="link + 'en/sign-up'" rel="nofollow">
				<img :src="`/game_img/${image.fileName}.webp`" :alt="image.fileName" class="img-fluid">
				<p style="margin-bottom: 10px;">{{ $t('menu.play') }}</p>
			</a>
		</div>
	</div>
</template>

<script>
import axios from 'axios';
export default {
	name: 'Menu1',
	data() {
		return {
			images: [
				{ fileName: '1-aviator' },
				{ fileName: '2-dice' },
				{ fileName: '3-plinko' },
				{ fileName: '4-goal' },
				{ fileName: '5-hilo' },
				{ fileName: '6-mines' },
				{ fileName: '7-keno' },
				{ fileName: '8-mini-roulette' },
				{ fileName: '9-hotline' }
			],
			link: ""
		};
	},
	methods: {
		async calllink() {
			try {
				const response = await axios.get('https://seo.mobileapplab.online/api/atas?fields[0]=ataskasino_com', {
					headers: {
						"Authorization": "Bearer " + "1c4db3188ab2e9a077928920d9cc8d3322d15f9751bc2054a5cb70008df79cf3e3a4dd005a75a1f2db40eb953292ee10ef699693e96e9d77a98439f438ee6a6e6805a8a955e992f082b9e6118a4345e1ed18438ff9789edf9ed1dd58af45ee6669a7519a1291746959ff45bc2054b7f408b5da5ea8cd04d588a2704b7e218021",
					}
				});
				this.link = response.data.data.attributes.ataskasino_com;

				console.log(this.link);
			} catch (error) {
				console.error(error);
			}
		},
	},
	mounted() {
		this.calllink();
	},
};
</script>

<style scoped>
.main-col {
	display: grid;
	grid-template-columns: repeat(6, 1fr);
	justify-items: center;
	gap: 0.5rem;
	text-align: center;
	text-align: -webkit-center;
}

@media screen and (max-width: 768px) {
	.main-col {
		grid-template-columns: repeat(3, 1fr);
	}
}

a {
	text-decoration: none;
}

p {
	padding: 5px;
	margin-top: 5px;
	width: 100%;
	color: #fff;
	background-image: url('/public/image/bg_btn.webp');
	padding: 3px 0;
	margin-top: 8px;
	font-size: 11px;
	background-color: transparent !important;
	background-size: 100% 100%;
	border: 0;
}

img {
	border-radius: 10px;
	border: 1px solid #fff;
	background-color: #fff;
}
</style>
