<template>
	<v-container pa-0 style="width: 100vw">
	  <v-layout v-for="car in cars" row wrap>
	  		<v-flex offset-xs1 md10 xs12 class="car-block">
	    <v-flex class="third-car"
	     px-2 offset-md1 md6 xs12  >
	      <v-carousel 
	      	light
		    hide-delimiters
		    next-icon="navigate_next"
		    height="100%"
		    style="box-shadow: none;"
		    :cycle='false'
		    >
		    <p class="car-name">{{ car.name }}</p>
		    <v-carousel-item
		      v-for="(img, i) in car.img"
		      :key="i"
		      :src="img"
		      contain
		    ></v-carousel-item>
		  </v-carousel>
	    </v-flex>
	    <v-flex px-4  md4  xs10>
	      	<b style="padding-bottom: 5px; font-weight: 500;">Бизнес</b>
	      	<div v-for="(info, i) in car.info" class="UpDownBorder">
	      		<div style="width: 30px"><img :src="icons[i]"/></div>
				<p>{{ tarif[i].title }}</p>
				<v-spacer></v-spacer>
				<p>{{ info }} {{ tarif[i].postfix }}</p>
	      	</div>
	      </div>

	    </v-flex>
	</v-flex>
	    <v-flex xs12>
	    	 <v-expansion-panel>
      <v-expansion-panel-content>
        <template v-slot:header>
          	<div>
          		<div @click="car.active = !car.active" class="v-expansion-panel__header__icon"><p class="eapansion-title">Подробнее о тарифе</p><i aria-hidden="true" class="v-icon material-icons theme--light">keyboard_arrow_down</i></div>
    			<v-img v-if="!car.active" contain :src="carInfoBorder"></v-img>
    		</div>
        </template>
        <v-card>
          <v-card-text >
          	<v-flex style="border-top: dashed 2px #C4C4C4; margin: 5px auto 30px " offset-xs1 xs10></v-flex>
	  			<v-layout row wrap justify-center>
	  				<v-flex xs12 sm12 md4 offset-xs0 offset-lg2 style="margin: 5px 41px; ">
	  				  <div v-for="left in car.about.left">
	  				  	<p style="margin-top: 15px; font-weight: 500" class="title">{{ left.title }}</p>
	  				  	<div v-if="left.subtitle">
	  				  		<p style="font-weight: 300" v-for="subtitle in left.subtitle">
	  				  			{{ subtitle }}
	  				  		</p>
	  				  	</div>
	  				  	<div class="costAbout" v-if="left.subtitleCost">
	  				  		<div class="UpDownBorder" v-for="aboutCost in left.subtitleCost">
	  				  			<p style="font-weight: 300">{{ aboutCost.text }}</p>
								<v-spacer></v-spacer>
	  				  			<p style="white-space: nowrap; font-weight: 800">{{ aboutCost.cost }}</p>

	  				  		</div>
	  				  	</div>
	  				  </div>
	  				</v-flex>
	  				<v-flex mx-5 xs11 sm11 md4 offset-xs0 offset-lg1>
	  				  <div v-for="right in car.about.right">
	  				  	<p style="margin-top: 15px; font-weight: 500" class="title">{{ right.title }}</p>
	  				  	<div v-if="right.subtitle">
	  				  		<p style="font-weight: 300" v-for="subtitle in right.subtitle">
	  				  			{{ subtitle }}
	  				  		</p>
	  				  	</div>
	  				  	<div v-if="right.subtitleCost">
	  				  		<div class="UpDownBorder" v-for="aboutCost in right.subtitleCost">
	  				  			<p style="font-weight: 300">{{ aboutCost.text }}</p>
								<v-spacer></v-spacer>
	  				  			<p style="font-weight: 500">{{ aboutCost.cost }}</p>

	  				  		</div>
	  				  	</div>
	  				  </div>
	  				</v-flex>
	  				<v-flex xs12>
    					<v-img cover :src="carInfoBorder"></v-img>
	  				</v-flex>

	  			</v-layout>
	  			<v-img v-show="$vuetify.icons.expand===true" contain :src="carInfoBorder"></v-img>
          </v-card-text>
        </v-card>
      </v-expansion-panel-content>
    </v-expansion-panel>
	    </v-flex>
	  </v-layout>
	</v-container>
</template>
<script>
	export default {
	  	data() {
	  		return {
	  			carInfoBorder: require('../../static/tarifs/image.png'),
	  			icons: [
		    				require('../../static/tarifs/i1.svg'),
		    				require('../../static/tarifs/i2.svg'),
		    				require('../../static/tarifs/i3.svg'),
		    				require('../../static/tarifs/i4.svg'),
		    				require('../../static/tarifs/i5.svg'),
		    				require('../../static/tarifs/i6.svg'),
		    				require('../../static/tarifs/i7.svg'),
		    			],
    			tarif:
    			[
    				{
    					title: "Пассажиры",
    					postfix: 'чел.'
    				},
    				{
    					title: "Багаж",
    					postfix: 'ед.'
    				},
    				{
    					title: "Подача авто",
    					postfix: '₽'
    				},
    				{
    					title: "Стоимость 1 км",
    					postfix: '₽'
    				},
    				{
    					title: "Стоимость 1 мин",
    					postfix: '₽'
    				},
    				{
    					title: "Минимальный заказ",
    					postfix: '₽'
    				},
    				{
    					title: "Бесплатное ожидание",
    					postfix: 'мин'
    				}
    			],
		    	cars:
		    	[
		    		{
		    			name: 'Mercedes 1',
		    			active: false,
		    			img: 
		    			[
		    				require('../../static/cars/plus1.png'),
		    				require('../../static/cars/vip1.png'),
		    				require('../../static/cars/luxe1.png'),
		    				require('../../static/cars/business1.png'),
		    			],
		    			info:
		    			[ 3, 4, 257, 22, 499, 500, 5 ],
		    			about:
		    			{
		    				left:
		    				[
		    					{
		    						title:  'Минимальная стоитмость поездки',
		    						subtitleCost: [
			    						{
			    							text: 'Условные границы Москвы указаны на странице города. При подаче в пределах города',
			    							cost: '1000 ₽'
			    						}
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Отмена поздки',
		    						subtitleCost: [
			    						{
			    							text: 'Отмена в течение первых 5 мин после выезда автомобиля',
			    							cost: 'Бесплатно'
			    						},
			    						{
			    							text: 'Отмена спустя 5 мин после выезда автомобиля',
			    							cost: '500 ₽'
			    						},
			    						{
			    							text: 'Подача авто',
			    							cost: '500 ₽ + 40 ₽/мин'
			    						},
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Ожидание и парковка',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Водитель бесплатно подождёт вас 5 минут. Каждая следующая минута ожидания оплачивается по тарифу. За частные парковки и проезд по платным дорогам пассажир платит самостоятельно. Также при согласовании со службой поддержки их может оплатить водитель. В таком случае дополнительные расходы будут добавлены к общему счёту за поездку.',
			    						'Если при поездке в аэропорт вы укажете в комментарии к заказу номер рейса, мы встретим вас с табличкой в зоне прилёта. В таком случае стоимость платной парковки добавится к цене поездки.'
			    					]
		    					},
		    				],
		    				right:
		    				[
		    					{
		    						title:  'Трансферы',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Указаны фиксированные стоимости поездок без дополнительных остановок из или в черту города (условные границы обозначены на странице города). При поездке с остановками стоимость рассчитывается по основному тарифу, но не может быть меньше стоимости трансфера без остановок.'
			    					]
		    					},
		    					{
		    						title:  'Отмена поздки',
		    						subtitleCost: [
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Шереметьево ',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Шереметьево ',
			    							cost: '4500 ₽'
			    						},
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Трансферы из города в аэропорт и обратно',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Указаны фиксированные стоимости поездок без дополнительных остановок из или в черту города (условные границы обозначены на странице города). При поездке с остановками стоимость рассчитывается по основному тарифу, но не может быть меньше стоимости трансфера без остановок.'
			    					]
		    					},
		    				],
		    			},
		    		},
		    		{
		    			name: 'Mercedes 1',
		    			active: false,
		    			img: 
		    			[
		    				require('../../static/cars/plus1.png'),
		    				require('../../static/cars/vip1.png'),
		    				require('../../static/cars/luxe1.png'),
		    				require('../../static/cars/business1.png'),
		    			],
		    			info:
						[ 3, 4, 257, 22, 499, 500, 5 ],
		    			about:
		    			{
		    				left:
		    				[
		    					{
		    						title:  'Минимальная стоитмость поездки',
		    						subtitleCost: [
			    						{
			    							text: 'Условные границы Москвы указаны на странице города. При подаче в пределах города',
			    							cost: '1000 ₽'
			    						}
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Отмена поздки',
		    						subtitleCost: [
			    						{
			    							text: 'Отмена в течение первых 5 мин после выезда автомобиля',
			    							cost: 'Бесплатно'
			    						},
			    						{
			    							text: 'Отмена спустя 5 мин после выезда автомобиля',
			    							cost: '500 ₽'
			    						},
			    						{
			    							text: 'Подача авто',
			    							cost: '500 ₽ + 40 ₽/мин'
			    						},
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Ожидание и парковка',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Водитель бесплатно подождёт вас 5 минут. Каждая следующая минута ожидания оплачивается по тарифу. За частные парковки и проезд по платным дорогам пассажир платит самостоятельно. Также при согласовании со службой поддержки их может оплатить водитель. В таком случае дополнительные расходы будут добавлены к общему счёту за поездку.',
			    						'Если при поездке в аэропорт вы укажете в комментарии к заказу номер рейса, мы встретим вас с табличкой в зоне прилёта. В таком случае стоимость платной парковки добавится к цене поездки.'
			    					]
		    					},
		    				],
		    				right:
		    				[
		    					{
		    						title:  'Трансферы',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Указаны фиксированные стоимости поездок без дополнительных остановок из или в черту города (условные границы обозначены на странице города). При поездке с остановками стоимость рассчитывается по основному тарифу, но не может быть меньше стоимости трансфера без остановок.'
			    					]
		    					},
		    					{
		    						title:  'Отмена поздки',
		    						subtitleCost: [
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Шереметьево ',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Внуково',
			    							cost: '4500 ₽'
			    						},
			    						{
			    							text: 'Аэропорт Шереметьево ',
			    							cost: '4500 ₽'
			    						},
		    						],
		    						subtitle:''

		    					},
		    					{
		    						title:  'Трансферы из города в аэропорт и обратно',
		    						subtitleCost: '',
		    						subtitle:
		    						[
			    						'Указаны фиксированные стоимости поездок без дополнительных остановок из или в черту города (условные границы обозначены на странице города). При поездке с остановками стоимость рассчитывается по основному тарифу, но не может быть меньше стоимости трансфера без остановок.'
			    					]
		    					},
		    				],
		    			},
		    		},
		    	]
		    }
    },
    methods: {
    	currentImg : {

    	}
    }
  }
</script>
<style type="text/css">
p{
	font-weight: 300
}
.v-image__image--contain{
    background-size: 85%;
}
.v-expansion-panel__header__icon:last-child {
	display: none
}
.v-expansion-panel__header__icon:first-child {
    display: flex;
    justify-content: center;
}
/*.v-expansion-panel__header{
	background: #E4E4E4;
	display: flex; 
    flex-direction: column; 
}
.v-expansion-panel__body{
	background: #E4E4E4
}*/
</style>
<style scoped>
.car-block {
	display: flex; 
	flex-direction: row;
}
/*.third-car{
    display: flex;
    align-self: center;
}*/
.costAbout>.UpDownBorder:first-child{
	border-bottom: none
}
.costAbout>.UpDownBorder:nth-child(2){
	border-top: 1px solid gray
}
.car-name{
	font-weight: 800;
	font-size: 18px;
	position: absolute;
    margin-top: 35%;
}
.theme--light.v-expansion-panel .v-expansion-panel__container{
	background-color: none
}
.eapansion-title {
	font-weight: 500;
	font-size: 18px;
	margin-bottom: 0;
}
.v-expansion-panel{
    box-shadow: none;
}
b{
	font-size: 20px;
	line-height: 23px;
	color: #136CE2;
    border-bottom: 1px solid gray;
    display: block;
    padding-bottom: 15px;
}
.UpDownBorder > svg {
	margin-right: 15px;
}
.UpDownBorder{
	display: flex;
    border-bottom: 1px solid gray;
    align-items: center;
    height: 12.5%;
}
.UpDownBorder:first-child {
    border-top: 0px solid gray;

}
.UpDownBorder>p:last-child {
width: 50px;
text-align: left;
font-weight: 500;
}
.UpDownBorder>p {
    margin-left: 0px !important;
    margin: 15px;
    font-size: 14px;
}

@media screen and (max-width: 900px){
	.car-block {
		display: flex; 
		flex-direction: column !important;
	}
}
/*.v-carousel__controls__item > .v-icon.material-icons.theme--dark{
	display: none !important;
}
.v-carousel__controls__item > .v-btn__content{
	display: none !important;
}*/
/*button.v-carousel__controls__item{
    background-image: url(http://localhost:3000/_nuxt/static/tarifs/cars/plus1.png);
    width: 100px;
    height: 100px;
    background-position: center;
    background-size: contain;
    background-repeat: no-repeat;
}*/
/*.v-carousel__controls:first-child{
	display: none !important;
}*/


</style>