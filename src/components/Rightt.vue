<template>
	<div style="height: 100%;" class="container-fluid">
		<div style="padding:10px ;" class="row ">
			<div class="col-6">
				<a href="https://www.ataskasino1.com/login/" rel="nofollow">
					<img width="100%" src="/image/login.gif" alt="login">
				</a>
			</div>
			<div class="col-6">
				<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
					<img width="100%" src="/image/register.gif" alt="register">
				</a>
			</div>

			<!--balance-->
			<div style="padding-top:10px ;" class="col-6">
				<p style="color: white;">{{ $t('right.baki') }}</p>
				<p style="color: #4DA5E8;"><b>0.00</b></p>
				<p style="color: #C0C0C0;">{{ $t('right.deposit') }}</p>
				<p style="color: #C0C0C0;"><b>RM5.00</b></p>
				<p style="color: #C0C0C0;">{{ $t('right.withdraw') }}</p>
				<p style="color: #C0C0C0;"><b>RM50.00</b></p>
			</div>
			<div style="padding-top:10px ;" class="col-6">
				<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
					<img style="padding-bottom: 5px;" width="100%" src="/image/deposit.gif" alt="deposit">
				</a>
				<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
					<img style="padding-bottom: 5px;" width="100%" src="/image/withdraw.gif" alt="withdraw">
				</a>
				<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
					<img style="padding-bottom: 5px;" width="100%" src="/image/refresh.gif" alt="refresh">
				</a>
			</div>


		</div>


		<p style="color: #FFD700;"><b>BCB88 SUPER BONUS <span class="free-hot">[FREE]</span></b></p>

		<div class="bonus">
			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<div class="btn-free">
					<img width="80%" src="/public/image/bcb_btn.gif" alt="bcb_button">
					<div class="btn-content">
						<p style="color: #FFD700;">FREE SHARE BONUS</p>
						<p>RM10</p>
					</div>

				</div>
			</a>

			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<div class="btn-shadow">
					<img width="80%" src="/public/image/bcb_btn.gif" alt="bcb_button">
					<div class="shadow-btn">
						<p>SLOT WELCOME BONUS</p>
						<p>50%</p>
					</div>

				</div>
			</a>
		</div>


		<p style="color: white;"><b>SLOT DEPOSIT BONUS <span class="free-hot">[HOT]</span></b></p>

		<div class="bonus">


			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<div class="btn-shadow">
					<img width="80%" src="/public/image/bcb_btn.gif" alt="bcb_button">
					<div class="shadow-btn">
						<p>DAILY FIRST BONUS</p>
						<p>20%</p>
					</div>

				</div>
			</a>

			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<div class="btn-shadow">
					<img width="80%" src="/public/image/bcb_btn.gif" alt="bcb_button">
					<div class="shadow-btn">
						<p>SLOT DEPOSIT BONUS</p>
						<p>3%</p>
					</div>

				</div>
			</a>

			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<div class="btn-shadow">
					<img width="80%" src="/image/bcb_btn.gif" alt="bcb_button">
					<div class="shadow-btn">
						<p>SLOT DEPOSIT BONUS</p>
						<p>8%</p>
					</div>

				</div>
			</a>
		</div>

		<div class="desktop">
			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<img style="border-radius: 10px;" width="100%" src="/image/free-credit-RM50_D.webp"
					alt="Download-APK-free-credit-RM50-D">
			</a>
		</div>

		<div class="mobile">
			<a href="https://www.ataskasino1.com/en/sign-up/" rel="nofollow">
				<img style="border-radius: 10px;" width="100%" src="/image/Download-APK-free-credit-RM50-M.webp"
					alt="Download-APK-free-credit-RM50-M">
			</a>
		</div>



	</div>







</template>

<script>
export default {
	name: 'Right',
};
</script>

<style scoped>
/* .bg_img {
	background: rgba(0, 0, 0, .3);
	border-right: 1px solid rgba(255, 255, 255, .5);
	height: 100vh;
} */

.right2 {
	margin-top: 25px;
	background-color: #FFF;
	border-radius: 10px;
	align-items: center;
	text-align: center;
	width: 100%;
}

.image_col {
	text-align: center;
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
}

.showmore {
	background-color: #EEE;
	color: #000;
	text-align: center;
	padding: 8px;
	font-size: 13px;
	line-height: 1;
	border-radius: 5px;
	width: 100%;
	box-shadow: 0 0 3px rgb(0 0 0 / 30%);
	border: 1px solid #ccc;
	cursor: pointer;
}

.showmore_col {
	padding-top: 10px;
	margin-bottom: 10px;
}

@media screen and (max-width:1100px) {
	.btn-content {
		font-size: 10px !important;
	}

	.shadow-btn {
		font-size: 10px !important;
	}
}

@media screen and (max-width:780px) {

	.btn-content {
		font-size: 8px !important;
	}

	.shadow-btn {
		font-size: 8px !important;
	}

	.text_sportlive {
		font-size: 15px !important;
	}

	.betnow {
		font-size: 10px;
	}

	.sportlive_col {
		padding: 11px 0px 10px 22px !important;
	}
}

@media screen and (max-width:576px) {

	.sportlive_col {
		padding: 11px 0px 10px 25px !important;
	}
}

@media screen and (max-width:426px) {
	.sportlive_col {
		padding: 30px 0px 10px 25px !important;
	}

	.text_sportlive {
		font-size: 14px !important;
	}
}

a {
	text-decoration: none;
}

@media screen and (max-width:376px) {

	.sportlive_col {
		padding: 22px 0px 10px 25px !important;
	}
}

p {
	margin: 0px;
}

.mobile {
	display: none;

}

.desktop {
	padding: 10px;
}



@media screen and (max-width:768px) {
	.desktop {
		display: none;
	}

	.mobile {
		display: block;
		padding-top: 10px;

	}

	.srceen_mobile {
		padding: 10px;
	}

	.btn-content {
		font-size: 12px !important;
	}

	.shadow-btn {
		font-size: 12px !important;
	}
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

.free-hot {
	animation: blink 1s infinite;
	/* 动画持续时间设置为1秒并无限次循环 */
	color: #EE1B1C;
}

.btn-free {
	position: relative;
	text-align: center;
}

.btn-content {
	position: absolute;
	top: 0px;
	left: 0px;
	font-weight: bold;
	color: white;
	text-align: center;
	font-size: 13px;
	width: 70%;
	padding-top: 10px;
	transform: translate(22%, 10%);
}

.btn-shadow {
	position: relative;
	text-align: center;
}

.shadow-btn {
	position: absolute;
	top: 0px;
	left: 0px;
	font-weight: bold;
	color: white;
	text-align: center;
	font-size: 13px;
	width: 70%;
	padding-top: 10px;
	transform: translate(22%, 10%);
}

.btn-shadow::before {
	content: "";
	position: absolute;
	left: 0;
	width: 100%;
	height: 100%;
	background: rgba(0, 0, 0, .6);
	z-index: 1;
}

.shadow-btn ::before {
	content: "";
	position: absolute;
	left: 0;
	width: 100%;
	height: 100%;

}



.bonus {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
}
</style>
