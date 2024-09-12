<template>
	<h1 style="color: white;padding-top: 10px;">
		{{ $t('BCB88.title') }}|
		{{ $t('BCB88.title2') }}
	</h1>
	<p>
		{{ $t('BCB88.1') }}
		<b>
			{{ $t('BCB88.2') }}
		</b>
		{{ $t('BCB88.3') }}
		<b>
			{{ $t('BCB88.4') }}
		</b>
		{{ $t('BCB88.5') }}
	</p>
	<br><br>

	<h3 style="color: white;">
		{{ $t('wheretojoin.title') }}
	</h3>
	<p>
		{{ $t('wheretojoin.1') }}
	</p>
	<ol style="color: white;">
		<li>
			{{ $t('wheretojoin.2') }}
			<b>
				{{ $t('wheretojoin.3') }}
			</b>
			{{ $t('wheretojoin.4') }}
		</li>

		<li>
			{{ $t('wheretojoin.5') }}
		</li>

		<li>
			{{ $t('wheretojoin.6') }}
			<b>
				{{ $t('wheretojoin.7') }}
			</b>
			{{ $t('wheretojoin.8') }}
		</li>
		<li>
			{{ $t('wheretojoin.9') }}
			<b>
				{{ $t('wheretojoin.10') }}
			</b>
			{{ $t('wheretojoin.11') }}
		</li>
		<li>
			{{ $t('wheretojoin.12') }}
			<b>
				{{ $t('wheretojoin.13') }}
			</b>
			{{ $t('wheretojoin.14') }}
		</li>
	</ol>


	<p>
		{{ $t('wheretojoin.15') }}
	</p>

	<br><br>

	<h3 style="color: white;">
		{{ $t('SpeedyandSecure.title') }}
	</h3>
	<p>
		{{ $t('SpeedyandSecure.1') }}
		<b>
			{{ $t('SpeedyandSecure.2') }}
		</b>
		{{ $t('SpeedyandSecure.3') }}
	</p>
	<p>
		{{ $t('SpeedyandSecure.4') }}
		<b>
			{{ $t('SpeedyandSecure.5') }}
		</b>
		{{ $t('SpeedyandSecure.6') }}
	</p>

	<br><br>

	<h3 style="color: white;">
		{{ $t('OnlineE-gamingProviders.title') }}
	</h3>
	<p>
		{{ $t('OnlineE-gamingProviders.1') }}
		<b>
			{{ $t('OnlineE-gamingProviders.2') }}
		</b>
		{{ $t('OnlineE-gamingProviders.3') }}
	</p>

	<ol style="color: white;">
		<li>
			<b>
				{{ $t('OnlineE-gamingProviders.4') }}
			</b>
			{{ $t('OnlineE-gamingProviders.5') }}
			<b>
				{{ $t('OnlineE-gamingProviders.6') }}
			</b>
			{{ $t('OnlineE-gamingProviders.7') }}
		</li>
		<li>
			<b>
				{{ $t('OnlineE-gamingProviders.8') }}
			</b>
			{{ $t('OnlineE-gamingProviders.9') }}
		</li>
		<li>
			<b>
				{{ $t('OnlineE-gamingProviders.10') }}
			</b>
			{{ $t('OnlineE-gamingProviders.11') }}
		</li>
		<li>
			<b>
				{{ $t('OnlineE-gamingProviders.12') }}
			</b>
			{{ $t('OnlineE-gamingProviders.13') }}
		</li>
	</ol>

	<p>
		{{ $t('OnlineE-gamingProviders.14') }}
	</p>

	<br><br>

	<h3 style="color: white;">
		{{ $t('BCB88Bonuses.title') }}
	</h3>
	<p>
		{{ $t('BCB88Bonuses.1') }}
		<b>
			{{ $t('BCB88Bonuses.2') }}
		</b>
		{{ $t('BCB88Bonuses.3') }}
	</p>

	<br>
	<a href="//www.dmca.com/Protection/Status.aspx?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e" rel="nofollow"
		title="DMCA.com Protection Status" class="dmca-badge"> <img
			src="https://images.dmca.com/Badges/dmca_copyright_protected150c.png?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e"
			alt="DMCA.com Protection Status" /></a>
	<br><br>

	<p style="font-weight: 700; color: #fff;">
		{{ $t('Footer.title') }}
	</p>

	<p style="color: #fff;">
		<a a :href="link" style="font-weight: 900; color:#FFD700;">{{
			$t('Footer.1') }}</a>
		| {{ $t('Footer.2') }}
	</p>

	<p style="padding-bottom: 80px; color: #fff;">
		<a a :href="link2" style="font-weight: 900;color:#FFD700; ">{{ $t('Footer.3')
			}}</a>
		| {{ $t('Footer.4') }}
	</p>

</template>
<script>
import axios from 'axios';
import { mapGetters } from 'vuex';
export default {
	name: 'Content',
	data() {
		return {

			link2: ""
		}
	},
	methods: {
		async calllink2() {
			try {
				const response = await axios.get('https://seo.mobileapplab.online/api/atas?fields[0]=atascasinobet_com', {
					headers: {
						"Authorization": "Bearer " + "1c4db3188ab2e9a077928920d9cc8d3322d15f9751bc2054a5cb70008df79cf3e3a4dd005a75a1f2db40eb953292ee10ef699693e96e9d77a98439f438ee6a6e6805a8a955e992f082b9e6118a4345e1ed18438ff9789edf9ed1dd58af45ee6669a7519a1291746959ff45bc2054b7f408b5da5ea8cd04d588a2704b7e218021",
					}
				});
				this.link2 = response.data.data.attributes.atascasinobet_com;

			} catch (error) {
				console.error(error);
			}
		},
	},
	mounted() {
		this.$store.dispatch('fetchLink');
		this.calllink2();
	},
	computed: {
		...mapGetters(['link'])
	}
}
</script>
<style>
h1 {
	font-size: 25px !important;
	font-weight: bolder !important;
}

h2 {
	font-size: 23px !important;
	font-weight: bolder !important;
}

h3 {
	font-size: 18px !important;
	font-weight: bolder !important;
}

p {
	color: white;
}
</style>
