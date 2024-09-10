<template>
	<div class="container-fluid">
		<div class="col-12 ">
			<div class="row ">
				<div class="bg_img">
					<div class="desktop">
						<a :href="link + 'en/sign-up'" rel="nofollow">
							<img style="border-radius: 15px;" width="100%"
								src="/public/image/Daily_unlimited_bonus_D.webp" alt="Daily_unlimited_bonus_D"> </a>
					</div>
					<div class="bonus">
						<a :href="link + 'en/sign-up'" rel="nofollow">
							<img style="border-radius:10px ;" width="100%" src="/image/bonus388.webp" alt="bonus388">
						</a>
					</div>

					<div class="table">
						<table class="table table-bordered">
							<thead>
								<tr>
									<th class="table_title" colspan="5">
										LIVE TRANSACTION
										<div class="live">
											<p style="margin: 0;">LIVE <span class="live_span"></span></p>
										</div>
									</th>
								</tr>
								<tr>
									<th style="background-color: #239809;" class="topup" colspan="2">TOP
										UP</th>
									<th style="background-color: #D02C27;" class="withdraw" colspan="3">
										WITHDRAW</th>
								</tr>
							</thead>
							<tbody>
								<tr v-for="(item, index) in tableData" :key="index">
									<td style="padding: 1px;">{{ item.topUpId }}</td>
									<td style="padding: 1px;color: #D0AD25;">{{ item.topUpAmount }}</td>
									<td style="padding:1px;">{{ item.withdrawId }}</td>
									<td style="padding: 1px;color: #D0AD25;">{{ item.withdrawAmount }}</td>
									<td style="padding: 1px;">{{ item.game }}</td>
								</tr>
							</tbody>
						</table>
					</div>



					<div class="srceen_mobile">

						<!--button bg-->
						<div style="padding-top: 10px;" class="btn_bg">
							<a :href="link + 'en/sign-up'" rel="nofollow">
								<img width="100%" src="/image/btn_bg.webp" alt="btn_bg">
							</a>

							<div style="position: absolute; bottom: 0px;" class="row">
								<div class="col-6 btn_left">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="95%" src="/image/btn_share.webp" alt="share">
									</a>
								</div>
								<div class="col-6 btn_right">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="95%" src="/image/btn_downline.webp" alt="downline">
									</a>
								</div>
								<div style="padding-top: 5px; padding-right: 3px;" class="col-6 btn_left">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="94%" src="/image/btn_copy.webp" alt="copy">
									</a>
								</div>
								<div style="padding-top: 5px; " class="col-6 btn_right">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="94%" src="/image/btn_more.webp" alt="more">
									</a>
								</div>

							</div>
						</div>
					</div>
					<!--owl carousel-->
					<div id="carouselExampleInterval" class="carousel slide" data-bs-ride="carousel">
						<div ref="carousel" id="carouselExampleInterval" class="carousel slide" data-bs-ride="carousel"
							@mousedown="startDrag" @mouseleave="endDrag" @mouseup="endDrag" @mousemove="onDrag">
							<div class="carousel-inner">
								<div class="carousel-item active" data-bs-interval="2000">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="100%" src="/image/banner1.webp" class="d-block w-100"
											alt="banner1" />
									</a>
								</div>
								<div class="carousel-item" data-bs-interval="2000">
									<a :href="link + 'en/sign-up'" rel="nofollow">
										<img width="100%" src="/image/banner2.webp" class="d-block w-100"
											alt="banner2" />
									</a>
								</div>
								<ol class="carousel-indicators">
									<li data-bs-target="#carouselExampleInterval" data-bs-slide-to="0"
										class="active single-dot"></li>
									<li data-bs-target="#carouselExampleInterval" data-bs-slide-to="1"
										class="single-dot"></li>
								</ol>
							</div>
						</div>
					</div>
					<!--sport live-->
					<div class="col-12 bg_test">
						<div class="row right2">
							<div class="col-3 text_sportlive">
								<div class="image_col">
									<img width="90%" src="/image/sportlive.webp" alt="sportlive1">
								</div>

								<p>{{ $t('right.manutd') }}</p>
							</div>
							<div class="col-6 text_sportlive">
								<p>{{ $t('right.starttime') }}</p>
								<p>17 Aug 2024</p>
								<p class="sportlive_text text_sportlive">03:00</p>
								<a :href="link + 'login'" class="betnow" rel="nofollow">{{
									$t('right.betnow') }}</a>
							</div>
							<div class="col-3 text_sportlive">
								<div class="image_col">
									<img width="90%" src="/image/spo.webp" alt="sportlive2">
								</div>
								<p>{{ $t('right.fulham') }}</p>
							</div>
						</div>

						<div class="showmore_col">
							<a :href="link + 'en/sport-live/'" rel="nofollow">
								<p class="showmore">{{ $t('right.showmore') }}</p>
							</a>
						</div>

					</div>


				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios';
export default {
	name: 'Left',
	data() {
		return {
			tableData: this.generateInitialData(),
			isDragging: false,
			startX: 0,
			scrollLeft: 0,
			link: ""
		};
	},
	mounted() {
		this.startUpdatingData();
		this.calllink();
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
		startDrag(e) {
			this.isDragging = true;
			this.startX = e.pageX - this.$refs.carousel.offsetLeft;
			this.scrollLeft = this.$refs.carousel.scrollLeft;
			this.$refs.carousel.style.cursor = 'grabbing';
		},
		endDrag() {
			this.isDragging = false;
			this.$refs.carousel.style.cursor = 'grab';
		},
		onDrag(e) {
			if (!this.isDragging) return;
			e.preventDefault();
			const x = e.pageX - this.$refs.carousel.offsetLeft;
			const walk = (x - this.startX) * 2; // Adjust scroll speed
			this.$refs.carousel.scrollLeft = this.scrollLeft - walk;
		},
		generateInitialData() {
			return Array.from({ length: 5 }, () => this.createRandomEntry());
		},
		startUpdatingData() {
			setInterval(() => {
				this.updateData();
			}, 10000); // 每5秒更新一次数据
		},
		createRandomEntry() {
			const generateRandomId = () => `60******${Math.floor(Math.random() * 1000).toString().padStart(3, '0')}`;
			const generateRandomAmount = (max) => `RM${(Math.random() * max).toFixed(2)}`;
			const games = ['KISS918', 'MAGA888', 'PUSSY'];

			return {
				topUpId: generateRandomId(),
				topUpAmount: generateRandomAmount(50), // 最高RM50
				withdrawId: generateRandomId(),
				withdrawAmount: generateRandomAmount(2000), // 最高RM500
				game: games[Math.floor(Math.random() * games.length)],
			};
		},
		updateData() {
			this.tableData = Array.from({ length: 5 }, () => this.createRandomEntry());
		}
	}
};
</script>

<style scoped>
.bg_img {
	padding-bottom: 100px;
}

@media screen and (max-width:768px) {
	.bg_img {
		padding-bottom: 0px;
	}
}

.carousel {
	padding-top: 10px;
}


.btn_bg {
	position: relative;
	padding-top: 10px;
}

.btn_left {
	text-align-last: end;
	padding-right: 0px;
}

.btn_right {
	text-align-last: start;
	padding-left: 0px;
}

.desktop {
	padding-top: 10px;
}

.mobile {
	display: none;
}

@media screen and (max-width:768px) {
	.desktop {
		display: none;
	}

	.mobile {
		display: block;
	}





	.table {
		padding-left: 10px;
		padding-right: 10px;
	}

	.bg_test {

		width: 100% !important;
	}
}

.bonus {
	padding-top: 10px;
}

.table {
	padding-top: 10px;
	margin: 0px;

}

.table tr {
	font-size: 9px;

}

.table th {
	background-color: black;
}

.table_title {
	color: #D3AB22;
	font-size: 12px;

}

.live {
	display: inline;
	float: right;
	margin: 0;
	background-color: red;
	color: white;

	padding: 0px 5px 0px 5px;
	border-radius: 5px;
}

.live_span {
	display: block;
	width: 8px;
	height: 8px;
	background: #fff;
	float: right;
	border-radius: 10px;
	margin: 5px 1px 0 3px;
}

tbody tr td {
	background-color: black;
	color: #fff;
}

@keyframes blink {
	0% {
		opacity: 1;
	}

	50% {
		opacity: 0;
	}

	100% {
		opacity: 1;
	}
}

.live {
	animation: blink 1s infinite;
	/* 动画持续时间设置为1秒并无限次循环 */
}

.topup {
	padding-bottom: 1px;
	padding-top: 1px;
	padding-left: 5px;
	background-color: #239809;
	color: #fff;
}

.withdraw {
	padding-bottom: 1px;
	padding-top: 1px;
	padding-left: 5px;
	background-color: #D02C27;
	color: white;
}

.bg_test {
	align-content: center;
	background-image: url(/image/right_bg2.webp);
	background-repeat: round;
	text-align: -webkit-center;
	width: 100%;
	margin-top: 10px;
	border-radius: 15px;
	padding-bottom: 10px;
	margin-bottom: 10px;
}

.right2 {
	margin-top: 25px;
	background-color: #FFF;
	border-radius: 10px;
	align-items: center;
	text-align: center;
	width: 95%;
}

.sportlive_col {
	padding: 26px 0px 10px 18px;
	text-align: -webkit-center;
	position: absolute;
}

.sportlive_text {
	font-size: 21px;
	color: #258D2D;
	font-family: digital-7;
}

.betnow {
	display: block;
	background: #4caf50;
	color: #fff;
	padding: 8px 0;
	line-height: 1;
	width: 72px;
	text-align: center;
	border-radius: 4px;
	margin: 5px auto 0;
	margin-bottom: 10px;
	text-decoration: none;
}

.showmore {
	background-color: #EEE;
	color: #000;
	text-align: center;
	padding: 8px;
	font-size: 13px;
	line-height: 1;
	border-radius: 5px;
	width: 95%;
	box-shadow: 0 0 3px rgb(0 0 0 / 30%);
	border: 1px solid #ccc;
	cursor: pointer;
	text-decoration: none;
}

a {
	text-decoration: none;
}

.showmore_col {
	padding-top: 10px;
	margin-bottom: 10px;
}

@media screen and (max-width:770px) {


	.text_sportlive {
		font-size: 15px !important;
	}

	.betnow {
		font-size: 10px;
	}


}



@media screen and (max-width:426px) {


	.text_sportlive {
		font-size: 14px !important;
	}
}

.bonus {
	display: none;
}

@media screen and (max-width:768px) {
	.bonus {
		display: block;
	}

	.desktop {
		display: none;
	}
}

.carousel-indicators .single-dot {
	width: 12px;
	height: 12px;
	background-color: #fff;
	border-radius: 50%;
	cursor: pointer;

}

.carousel-indicators li {
	width: 12px;
	height: 12px;
	background-color: #fff;
	border-radius: 50%;
	cursor: pointer;
	transition: background-color 0.3s;
}

.carousel-indicators li.active {
	background-color: #fffcfc;
}

/* Remove default list numbering */
.carousel-indicators ol {
	list-style: none;
	padding: 0;
	margin: 0;
}

.carousel-indicators li::before {
	content: none;
}

.carousel-indicators li::marker {
	display: none !important;
	color: rgba(0, 0, 0, 0);
}

.carousel-indicators {
	z-index: 1;
}
</style>