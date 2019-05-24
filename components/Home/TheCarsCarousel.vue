<template>
	<v-layout row wrap>
      <v-flex v-for="(car,i) in cars"
	      	 :key="i" xs12>
		<div :class="car.pos+' coolCar'">
		    <p><b>{{ car.text }}</b></p>
	    	<img :class="car.pos" :src="car.src"></img>
		</div>
		<div v-show="count === i" class="tarifs" style="width: 19vw;">
	      	<v-btn outline color="black">Тарифы</v-btn>
	      	<p>{{car.mark}}</p>
	    </div>
      </v-flex>
      <div class="carousel-icons">
	      <v-icon @click="completePrev">arrow_back_ios</v-icon>
	      <v-icon @click="completeNext">arrow_forward_ios</v-icon>
      </div>
	</v-layout>
</template>

<script>
import Vuetify, {
  VBtn,
} from 'vuetify/lib'
  export default {
    data () {
      return {
        cars: [
          {
            src: require('../../static/cars/luxe1.png'),
            pos: 'first',
            text: 'VIP',
            mark: 'Mercedes-Benz S-class BMW 7 Series',
            current: false
          },
          {
            src: require('../../static/cars/vip1.png'),
            pos: 'second',
            text: 'Премиум',
            mark: 'Premium wow car',
            current: true
          },
          {
            src: require('../../static/cars/plus1.png'),
            pos: 'third',
            text: 'Минивен',
            mark: 'Miniven wow car',
            current: false
          },
          {
            src: require('../../static/cars/business1.png'),
            pos: 'four',
            text: 'Бизнес',
            mark: 'Buisness wow car',
            current: false
          }
        ],
        count: 0
      }
    },
    mounted() {
    },
    methods: {
    	completeNext﻿: function () {
			var tl = new TimelineMax;
			tl.add(
		    		TweenLite.to('.first.coolCar', 1, {className: "four coolCar"}),
		    		TweenLite.to('.second.coolCar', 1, {className: "third coolCar"}),
		    		TweenLite.to('.third.coolCar', 1, {className: "first coolCar"}),
		    		// TweenLite.to('.four.coolCar', 1, {className: "second coolCar"})
		    		TweenLite.to('.four.coolCar', 1, {className: "second coolCar", onComplete: this.currentCar})
    			);

		},
		completePrev: function () {
			var tl = new TimelineMax;
			tl.add(
		    		TweenLite.to('.first.coolCar', 1, {className: "third coolCar"}),
		    		TweenLite.to('.second.coolCar', 1, {className: "four coolCar"}),
		    		TweenLite.to('.third.coolCar', 1, {className: "second coolCar"}),
		    		// TweenLite.to('.four.coolCar', 1, {className: "first coolCar"})
		    		TweenLite.to('.four.coolCar', 1, {className: "first coolCar", onComplete: this.currentCar})
    			);
		},
		currentCar: function () {
			let current = document.querySelector('.second');
			let link = window.location.href;
			let currentCar = this.cars.find((element, i, array) => {
				if (current.src === link + element.src.substring(1)) {
					this.count = i;
					console.log(i);
				}
			})
		}
	}
}
</script>

<style lang="stylus" scoped>

.layout
	-webkit-justify-content center
	justify-content center

.coolCar
	position absolute
	background-size: auto !important;
.coolCar > img
	height auto

.coolCar.first
	width: 15%
	margin-top 5vh
	right: -5vw !important
.coolCar.second
	width: 34%
	margin-top 30vh
	right: 49vw !important
.coolCar.third
	width: 25%
	margin-top 25vh
	right 10vw !important
.coolCar.four
	width: 20%
	margin-top 5vh
	right 88vw !important


img
	width: 100%
	position absolute
	background-size: auto !important;
</style>

<style lang="stylus" scoped>
.carousel-icons
    margin-top: 8%
    z-index: 99;
    .v-icon
	    font-size: 40px
	    &:first-child
    	    margin-right: 15px
</style>

<style lang="stylus" scoped>
.tarifs {
    display: flex;
    flex-direction: row-reverse;
	position: absolute;
    margin-top: 60vh !important;
    right: 57vw !important;
    width: 150px;
}
	p{
		font-size: 21px;
    }
</style>

<style scoped>
@media screen and (max-width: 900px){
	.tarifs {
	    display: flex;
	    flex-direction: column-reverse;
		position: absolute;
	    margin-top: 50vh !important;
	    right: 0vw !important;
	    width: 100vw !important;
	    text-align: center;
    }
    p{
		font-size: 21px;
    }
}
</style>