<template>
	<v-layout row wrap>
      <v-flex v-for="(item,i) in items"
	      	 :key="i" xs12>
    	<img :src="item.src"
	      	 :class="item.pos"
	      	 ></img>
		<div v-show="count === i" class="tarifs" style="width: 19vw;">
	      	<v-btn outline color="black">Тарифы</v-btn>
	      	<p>{{item.text}}</p>
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
        items: [
          {
            src: require('../../static/cars/luxe1.png'),
            pos: 'first',
            text: 'Mercedes-Benz S-class BMW 7 Series',
            current: false
          },
          {
            src: require('../../static/cars/vip1.png'),
            pos: 'second',
            text: 'Mercedes-Benz S-class BMW 7 Series 2',
            current: true
          },
          {
            src: require('../../static/cars/plus1.png'),
            pos: 'third',
            text: 'Mercedes-Benz S-class BMW 7 Series 3',
            current: false
          },
          {
            src: require('../../static/cars/business1.png'),
            pos: 'four',
            text: 'Mercedes-Benz S-class BMW 7 Series 4',
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
		    		TweenLite.to('.first', 1, {className: "four"}),
		    		TweenLite.to('.second', 1, {className: "third"}),
		    		TweenLite.to('.third', 1, {className: "first"}),
		    		TweenLite.to('.four', 1, {className: "second", onComplete: this.currentCar})
    			);

		},
		completePrev: function () {
			var tl = new TimelineMax;
			tl.add(
		    		TweenLite.to('.first', 1, {className: "third"}),
		    		TweenLite.to('.second', 1, {className: "four"}),
		    		TweenLite.to('.third', 1, {className: "second"}),
		    		TweenLite.to('.four', 1, {className: "first", onComplete: this.currentCar})
    			);
		},
		currentCar: function () {
			let current = document.querySelector('.second');
			let link = window.location.href;
			let currentCar = this.items.find((element, i, array) => {
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
	
img
	width: 10%
	position absolute
	background-size: auto !important;
img.first
	margin-top 0vh
	right: -6vw !important
	width: 10%
	opacity: 1
img.second
	margin-top 20vh
	right: 55vw !important
	width: 40%
	opacity: 1
img.third
	margin-top 25vh
	right 8vw !important
	width: 25%
	opacity: 1
img.four
	margin-top 0vh
	right 95vw !important
	width: 10%
	opacity: 1
img.away-four
	margin-top 0vh
	right 110vw !important
	width 10%
	opacity 0
img.away-first
	margin-top 0vh
	right -10vw !important
	width 10%
	opacity 0
</style>

<style lang="stylus" scoped>
.carousel-icons
    margin-top: 8%
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