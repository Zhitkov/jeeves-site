<template>
	<v-container fluid style="background-size: 100% 100vh; background-position: center -25vh; padding: auto 0; min-width: 100vw; margin-bottom: 165px; height: 100vh;" >
	  <v-layout column wrap >
	    <v-flex xs12>
	    <v-flex offset-md2 md8 xs12 class="text-c third-container">
	      <h1 class="third-title">K Вашим услугам наш парк новых авто,</h1>
	      <h3 class="third-subtitle">которые мы содержим в безупречной чистоте и таком же техническом состоянии.</h3>
	      <p class="third-text">Никакого брендирования.</p>
	    </v-flex>
	    </v-flex>
	    <TheCarsCarousel style="margin-bottom: 20vh;"/>
	    <div class="static">
	    <v-flex offset-xs2 xs5 style="display:flex; margin-top: 27%;">
			<v-flex offset-xs2 xs4><p style="font-weight: 100;">Mercedes-Benz S-class BMW 7 Series</p></v-flex>
			<v-flex offset-xs1 xs5><v-btn to="/tarifs" style="margin: auto 15%;width: 70%; height: 70%;" outline color="black">Тарифы</v-btn></v-flex>
		</v-flex>
	    </div>
	  </v-layout>
	</v-container>
</template>

<script>
import TheCarsCarousel from '~/components/Home/TheCarsCarousel.vue'
import { TweenMax, TweenLite, Power2 } from 'gsap';
export default {
  components: {
    TheCarsCarousel,
  }
}
</script>

<style lang="stylus" scoped>
.container
	height 100vh
	width  100vw
	background-image url('../../static/Home/road.png') 
	.third-container
		height 55%
		margin-top: 2%
		.third-title
			font-weight: 500
			font-size 32px
		.third-subtitle
			font-weight: 500
			font-size 21px
			max-width 50%
			display: inline-block;
		.third-text
			font-weight: 500
			font-size 21px
			font-weight 100 
</style>

<style scoped>
@media screen and (max-width: 900px){
	.third-title {
		font-size: 21px !important;
	}
	.container {
		background-position: 1px -30vh !important;
	    height: 110vh;
	}
}
</style>
