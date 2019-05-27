<template>
	<v-parallax class="parallax-screen" cover :src="bg" :lazy-src="bg">
		<v-layout style="padding-top: 20vh; background: linear-gradient(to top, #000 0%, #000000a0 1%, #000000a0 100%) !important;" row wrap>
		  <v-flex offset-xs1 xs10 md5>
		  <v-flex offset-xs1 xs10 offset-md2 md9>
		    <p class="title neue">Корпоративное Обслуживание</p>
		    <p class="text">
		    	Давно выяснено, что при оценке дизайна и композиции читаемый текст мешает сосредоточиться. Lorem Ipsum используют потому, что тот обеспечивает более или менее стандартное заполнение шаблона, а также реальное распределение букв и пробелов в абзацах, которое не получается при простой дубликации "Здесь ваш текст.. Здесь ваш текст.. Здесь ваш текст.." Многие программы электронной вёрстки и редакторы HTML используют Lorem Ipsum в качестве текста по умолчанию, так что поиск по ключевым словам "lorem ipsum" сразу показывает, как много веб-страниц всё ещё дожидаются своего настоящего рождения. За прошедшие годы текст Lorem Ipsum получил много версий.
		    </p>
		  </v-flex>
		</v-flex>
		  <v-flex xs12 md5>
		  <v-flex offset-xs1 xs10 offset-md1 md7>
		    <p class="title neue">Заявка</p>
		    <Form :aboutBuisness="true"/>
		</v-flex>
		  </v-flex>
		  <v-flex style="margin-top: 100px;" offset-xs1 xs10>
		    <AboutVector :aboutBuisness="true"/>
		  </v-flex>
		</v-layout>
	</v-parallax>
</template>

<script>
import AboutVector from '~/components/layouts/AboutVector.vue'
import Form from '~/components/layouts/Form.vue'

export default {
	components: {
      AboutVector,
      Form
    },
	data () {
		return {
			bg: require('../../static/buisness/bg.png'),
		}
	}
}
	
</script>
<style scoped>
.parallax-screen{
  width: 100vw;
  height: auto !important;
}
.title{
	font-size: 38px !important;
    text-align: center;
}
.text{
	font-size: 18px;
	font-weight: 100;
    text-align: justify;
}
</style>
<style>
	.v-parallax__content {
	padding: 0 !important;
}
</style>
