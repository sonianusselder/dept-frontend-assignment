<template>
	<section class="section section__clients clients">
		<div class="clients__description">
			<h3>Clients</h3>
			<p>We value a great working relationship with our clients above all else. It’s why they often come to our parties. It’s also why we’re able to challenge and inspire them to reach for the stars.</p>
		</div>
		<div class="clients__logo-container">
			<div v-for="(client, index) in clients" :key="index" class="clients__logo">
				<img :src="client.url">
			</div>
		</div>
	</section>	
</template>

<script>
// import clientLogo from '~/components/elements/client-logo.vue';
export default {
	components: {
		// clientLogo
	},
	props: ['caseClient', 'caseTitle', 'caseLink', 'caseType'],
	data () {
        return {
            clients: [
                { url: require('~/static/images/clients/ABN.png')},
                { url: require('~/static/images/clients/Adidas.png')},
                { url: require('~/static/images/clients/KLM.png')},
                { url: require('~/static/images/clients/Microsoft.png')},
                { url: require('~/static/images/clients/Mona.png')},
                { url: require('~/static/images/clients/Nivea.png')},
                { url: require('~/static/images/clients/NN.png')},
                { url: require('~/static/images/clients/Oxxio.png')},
				{ url: require('~/static/images/clients/Pathe.png')},
				{ url: require('~/static/images/clients/Tomtom.png')},
				{ url: require('~/static/images/clients/Transavia.png')},
				{ url: require('~/static/images/clients/Triumph.png')},
				{ url: require('~/static/images/clients/Unilever.png')},
				{ url: require('~/static/images/clients/Walibi.png')},
				{ url: require('~/static/images/clients/Zalando.png')},
				{ url: require('~/static/images/clients/Ziggo.png')},
            ]
		}
	}
};
</script>

<style lang="scss">
@import '~tools';

.clients  {
	background-color:color(PaleGrey);
	justify-content: center;

	&__description {
		text-align: center;
		width: 40%;
		@media #{$medium-down} {
			width: 100%;
		}
	}

	&__logo-container {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		width: 71%;
		padding: 80px 0 20px;
		@media #{$medium-down} {
			width: 100%;
		}
	}
	&__logo {
		width: 25%;
		height: 126px;
		position: relative;

		@media #{$medium-down} {
			width: 33.33%;
			height: 86px;
			&:nth-child(n+7) {
				display: none;
			}
		}

		img {
			position: absolute;
			transform: translate(-50%, -50%);
			top: 50%;
			left: 50%;
			max-width: 100px;
			@media #{$medium-down} {
				max-width: 60px;
			}
		}

	}
}
</style>