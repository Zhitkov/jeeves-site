
<template>
	<v-container fluid style="background-size: 100% 100vh; background-position: center -25vh; padding: auto 0" >
	  <v-layout row wrap>
	    <v-flex xs12 class="text-c third-container">
	      <h1 class="third-title">K Вашим услугам наш парк новых авто,</h1>
	      <h3 class="third-subtitle">которые мы содержим в безупречной чистоте и таком же техническом состоянии.</h3>
	      <p class="third-text">Никакого брендирования.</p>
	    </v-flex>
	    <TheCarsCarousel/>
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
			font-size 2vw
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