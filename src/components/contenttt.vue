<template>
	<div style="padding-top: 10px;" class="main-col container">
		<div v-for="(image, index) in images" :key="index" class="col">
			<a :href="`https://www.ataskasino.com/en/sign-up/`" rel="nofollow">
				<img :src="`/game_img/${image.fileName}.webp`" :alt="image.fileName" class="img-fluid">
				<p style="margin-bottom: 10px;">{{ $t('menu.play') }}</p>
			</a>
		</div>
	</div>
</template>

<script>
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
			]
		};
	}
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
