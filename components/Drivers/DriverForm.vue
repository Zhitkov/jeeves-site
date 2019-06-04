<template>
	<v-layout style="display: flex; justify-content: center;" row wrap>
		<div style="flex-direction: column;" class="static">
			<div style="display: flex;">
		<v-flex pl-5 offset-md3 md4 offset-xs1 xs10 style="display: flex; justify-content: center;">
	      <v-menu nudge-bottom="30" nudge-right="65" :close-on-click="menuOpen" :close-on-content-click="menuOpen" bottom left>
	      		<div @click="menuOpen = !menuOpen" slot="activator" class="driver-about">
	      			<p class="linkText">Требования к атомобилям</p>
	      			<v-icon>expand_more</v-icon>
					<div style="margin-top: 22px; margin-left: 87px;" v-if="!menuOpen" class="tooltip-arrow-up"></div>
	      		</div>
	      	<v-card class="superCard">
	      		<v-card-tile style="background: white !important;">
	      		<v-card-tile-title style="">
	      			<ul class="forCars">
	      				<v-icon @click="menuOpen = !menuOpen" class="clear">clear</v-icon>
	      				<li>Бизнес <v-spacer></v-spacer> <b> Mercedes E-Class, BMW 5</b></li>
	      				<li>Бизнес <v-spacer></v-spacer> <b> Mercedes E-Class, BMW 5</b></li>
	      				<li>Бизнес <v-spacer></v-spacer> <b> Mercedes E-Class, BMW 5</b></li>
	      				<li>Бизнес <v-spacer></v-spacer> <b> Mercedes E-Class, BMW 5</b></li>
	      				<b class="about">Возраст авто не старше 3-х лет, только черный и белый цвета, салон кожа или кожзаменитель, отсутствие каких либо дефектов.</b>
	      			</ul>
	      		</v-card-tile-title>
	      	</v-card-tile>
	      </v-card>
	  </v-menu>
	</v-flex>
	 <v-flex offset-md1 md2 offset-xs1 xs10 style="display: flex; justify-content: center;">

	  	<v-menu id="app2" nudge-bottom="30" nudge-left="70" :close-on-click="menuOpen2" :close-on-content-click="menuOpen2" bottom right>
	      		<div @click="menuOpen2 = !menuOpen2" slot="activator" class="driver-about">
	      			<p class="linkText">Требования к водителям</p> 
		  			<v-icon>expand_more</v-icon>
					<div style="margin-top: 22px; margin-left: 82px;" v-if="!menuOpen2" class="tooltip-arrow-up"></div>
	      		</div>
	      	<v-card class="superCard">
	      		<v-card-tile style="background: white !important;">
	      		<v-card-tile-title style="">
	      			<ul class="forDrivers">
	      				<v-icon @click="menuOpen2 = !menuOpen2" class="clear">clear</v-icon>
	      				<b class="about">Давно выяснено, что при оценке дизайна и композиции читаемый текст мешает сосредоточиться. Lorem Ipsum используют потому, что тот обеспечивает более или менее стандартное заполнение шаблона,</b>
	      				<ol>
	      					<li>Многие думают, что Lorem Ipsum - взятый с потолка псевдо-латинский набор слов, но это не совсем так.</li>
	      					<li>Его корни уходят в один фрагмент классической латыни 45 года н.э., то есть более двух тысячелетий назад.</li>
	      					<li>Ричард МакКлинток, профессор латыни из колледжа Hampden-Sydney, штат Вирджиния, взял одно из самых странных слов в Lorem Ipsum.</li>
	      					<li>Есть много вариантов Lorem Ipsum, но большинство из них имеет не всегда приемлемые модификации, например, юмористические вставки или слова, которые даже отдалённо не напоминают латынь.</li>
	      					<li> Если вам нужен Lorem Ipsum для серьёзного проекта, вы наверняка не хотите какой-нибудь шутки, скрытой в середине абзаца.</li>
	      					<li>Многие думают, что Lorem Ipsum - взятый с потолка псевдо-латинский набор слов, но это не совсем так.</li>
	      				</ol>
	      			</ul>
	      		</v-card-tile-title>
	      	</v-card-tile>
	      </v-card>
	  </v-menu>
</v-flex>
</div>
<div style="display: flex;">
<v-flex xs10 md7>
	<v-flex md9 xs12 >
		<v-select
		class='driver-select'
		:items="cities"
		label="Город"
		outline
		background-color="#fff"
		></v-select>
	</v-flex>
	<v-flex md9 xs12 >
		<v-select
		class='driver-select'
		:items="workers"
		label="Желаемый тип рабочих"
		outline
		background-color="#fff"
		></v-select>
	</v-flex>
	<v-flex md9 xs12 >
		<v-text-field
		class="form-white"
		label="ФИО"
		outline
		></v-text-field>
	</v-flex>
	<v-flex md9 xs12 >
		<v-text-field
		class="form-white"
		outline
		v-model="email"
		:rules="[rules.required, rules.email]"
		label="E-mail"
		></v-text-field>
	</v-flex>
	<v-flex md9 xs12 style="display: flex;">
		<PhoneForm class="driver-phone" :aboutBuisness="true" style="width: 50%;"/>
		<v-btn color="primary" large style="width: 50% !important; margin-top: 2px; border-radius: 3px;">Отправить заявку</v-btn>
	</v-flex>
</v-flex>
<v-flex xs4 class="steps">
	<v-flex class="step" xs1 >
		<p class="step-title"> Заявка на сайте </p>
		<v-text-field
		class="form-white"
		label="1"
		outline
		disabled
		></v-text-field>
	</v-flex>
	<v-flex class="step" xs1 >
		<p class="step-title"> Собеседование </p>
		<v-text-field
		class="form-white"
		label="2"
		outline
		disabled
		></v-text-field>
	</v-flex>
	<v-flex class="step" xs1 >
		<p class="step-title"> Тест на вождение и знание города </p>
		<v-text-field
		class="form-white"
		label="3"
		outline
		disabled
		></v-text-field>
	</v-flex>
	<v-flex class="step" xs1 >
		<p class="step-title"> Внутреннее обучение </p>
		<v-text-field
		class="form-white"
		label="4"
		outline
		disabled
		></v-text-field>
	</v-flex>
	<v-flex class="step" xs1 >
		<p class="step-title"> Вы в команде </p>
		<v-text-field
		class="form-white"
		label="5"
		outline
		disabled
		></v-text-field>
	</v-flex>
</v-flex>
</div>
</div>
</v-layout>
</template>


<script>
	import PhoneForm from '~/components/layouts/PhoneForm.vue'

	export default {
		components: {
			PhoneForm,
		},
		data: () => ({
			workers: ['Курьер', 'Водитель'],
			cities: ['Москва', 'Санкт-Петербург'],
			rules: {
				email: value => {
					const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
					return pattern.test(value) || 'Invalid e-mail.'
				},
				required: value => !!value || 'Required.',
			},
			menuOpen: true,
			menuOpen2: true
		}),
			props:['aboutBuisness'],
	}
</script>

<style type="text/css">
.driver-select .v-input__slot{
	border-color: gray !important
}
.steps {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.step{
    min-width: 54px !important;
}
	.step .v-input__slot label{
		color: #000 !important;
	}
	.step .v-input__slot{
		padding: 0 20px !important;
		border-radius: 3px !important;
	}
	.step-title{
		font-weight: 500;
		font-size: 20px;
		position: absolute;
		margin-left: 80px;
	    margin-top: 13px;
	}
	.driver-phone .v-input__slot {
		    border: 1px solid gray !important;
	}

</style>
<style scoped>
	.driver-about > p {
		margin-bottom: 0px;
	}
	.superCard {
		width: 40vw;
		max-width: 650px;
		padding: 30px;
		height: 430px;
	}
	.driver-about{
		display: flex;
		-webkit-justify-content: center;
		        justify-content: center;
		margin-bottom: 30px;
	}
	.forCars {
		background: white;
		width: 90%;
		text-align: center;
	}
	.forCars ul  {
		width: 100%;
	}
	.forCars li  {
		text-decoration: none;
		list-style: none;
		width: 100%;
		display: flex;
	    margin-left: 0px !important;
	    padding: 15px;
	    font-size: 14px;
	    border-bottom: 1px solid gray;
	}
	ul > li:nth-child(5)  {
	    margin-bottom: 20px !important;
	}
	.about {
		color: #2196f3 !important;
	}
	.forDrivers > ol > li {
		font-weight: 300;
		font-size: 14px;
		line-height: 16px;
		margin: 10px 0;
	}

    div.tooltip-arrow-up {
		/*border-left: 10px solid #00000000;
		border-right: 10px solid #00000000;
		border-bottom: 10px solid red;*/
		width: 15px;
		height: 15px;
		transform: rotate(45deg);
		background-color: #FFF;
		box-shadow: inset 1px 1px 1px 0px #000000a0;
		position: absolute;
		z-index: 9999999;
    }
    .clear{
    	position: absolute; 
    	right: 10px; 
    	top: 10px; 
    	cursor: pointer
    }
    .v-menu__content.theme--light.menuable__content__active{
		box-shadow: 0px 0px 2px 0px;
		width: 40vw;
		max-width: 650px
    }

@media screen and (max-width: 900px){
	    .steps {
	    display: flex;
	    flex-direction: column;
	    align-items: center;
	}
	.v-menu__content.theme--light.menuable__content__active {
		margin-top: .2vh !important;
		left: 0vw !important;
		width: 100% !important;
	}
	.superCard {
		left: 0vw;
		width: 100vw;
		max-width: 100vw;
		padding: 0px;
		height: 100%;
	}
}
</style>