<template>
	  <v-layout style="margin: 45px auto;" row wrap justify-start>
	    <v-flex 
	    xs10 sm10 md6 offset-xs1 offset-lg2>
	      <p class=" neue"> Тарифы </p>
	      <p style="font-size: 18px; font-weight: 100" class="subtitlte">
	      	Давно выяснено, что при оценке дизайна и композиции читаемый  текст мешает 
			сосредоточиться. Lorem Ipsum используют потому, что тот обеспечивает более 
			или менее стандартное заполнение шаблона, а также реальное распределение 
			букв и пробелов в абзацах, которое не получается при простой дубликации 
			"Здесь ваш текст.
	      </p>
	    </v-flex>
	    <v-flex 
	    xs10 sm10 md3 offset-xs1 offset-lg2 >
		      <p style="display: inline-block; margin-right: 15px" class=" linkText neue"> Москва </p>
		      <p style="display: inline-block" class=" linkText neue"> Санкт-Петербург </p>
		      <!-- <p class="link linkText"> Условные границы города </p> -->


		      <v-tooltip bottom>
		      	<template v-slot:activator="{ on }">
		      		<p class="link linkText" v-on="on"> Условные границы города </p>
		      	</template>
		      	<span>Bottom tooltip</span>
		      </v-tooltip>


		    </v-flex>
	  </v-layout>
</template>
<style type="text/css">
.neue{
	font-size: 36px;
	line-height: 36px;
	font-weight: 100;
	margin-top: 11px;
	margin-bottom: 20px;
}
</style>