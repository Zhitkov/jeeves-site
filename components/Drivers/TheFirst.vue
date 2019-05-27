<template>
  <v-layout class="full-screen" row wrap>
    <v-img class="parallax-screen change" dark :lazy-src="require('../../static/Drivers/bg.png')" cover :src="require('../../static/Drivers/bg.png')" gradient="to top right, rgba(1, 22, 46, 0.2), rgba(1, 22, 46, 0.2)">
      <v-flex offset-xs1 xs2>
        <img style="padding-bottom: 42px; float: right;" :src="logo">
      </v-flex>
    </v-img>
    <v-flex offset-md2 md8 offset-xs1 xs10>
      <p  class="driver-title"> Зарабатывайте с JEEVES </p>
    </v-flex>
    <v-flex style="margin-top: 0px !important;" class="thin" offset-md2 md5 offset-xs1 xs10>
      <b style="color: #136CE2;">JEEVES</b> — это не просто личный водитель на премиальном автомобиле,
    это личный ассистент!</v-flex>
    <v-flex class="thin" offset-md2 md5 offset-xs1 xs10>
      Основным принципом работы компании, является высочайший уровень предоставляемых услуг. С нашей помощью пассажиры получают высококлассный сервис, а водители — достойно зарабатывают.
      Наша главная ценность и гордость  — это наши сотрудники.
    </v-flex>
    <v-flex class="thin" offset-md2 md5 offset-xs1 xs10>
      Принимаем в команду Водителей на автомобили нашего парка,
      а так же  приглашаем к сотрудничеству парки и Водителей с личными
      авто бизнес/премиум класса.
    </v-flex>
    <v-flex offset-md2 md8 offset-xs1 xs10>
      <p class="driver-title"> Преимущества работы с JEEVES </p>
    </v-flex>
    <v-flex offset-xs1 xs10>
      <AboutVector style="max-width: 1500px;" :aboutBuisness="false"/>
    </v-flex>
    <v-flex offset-md2 md8 offset-xs1 xs10>
      <p class="driver-title"> Станьте партнёром JEEVES прямо сейчас </p>
    </v-flex>
    <DriverForm/>
  </v-layout>
</template>

<script>
import AboutVector from '~/components/layouts/AboutVector.vue'
import DriverForm from '~/components/Drivers/DriverForm.vue'

  export default {
    components: {
      AboutVector,
      DriverForm

    },
    data () {
      return {
        logo: require('../../static/logos/logo2.png'),
      }
    },
    methods: {
    //   completeNext﻿: function () {
    //   var tl = new TimelineMax;
    //   tl.add(
    //         TweenLite.to('.opa', 1, {opacity: 1}),
    //       );

    // },
  }
}
</script>

<style lang="stylus" scoped>
.v-responsive__content
  align-self: flex-end;
.full-screen
  width 100vw
div[data-v-00bd8e1c].container
  align-items: flex-end !important
.parallax-screen
  width 100vw
  height 65vh !important
  .container
    align-content: center;
    align-items: center;
    align-self: center;
    display: flex;
.First-text
  text-align center 
.downloads
  margin-bottom 10vw 
</style>
<style scoped>
.driver-title {
  font-weight: 500;
  font-size: 30px;
  margin-bottom: 75px;
  margin-top: 55px;
}
.thin {
  font-size: 21px !important;
  font-weight: 100;
  margin-top: 35px;
}
@media screen and (max-width: 900px){
  .driver-title {
  font-weight: 500;
  font-size: 23px;
  margin-bottom: 75px;
  margin-top: 55px;
}
  .First-text{
    font-size: 20px; 
    margin: 5% 10% 1%;
  }
  .parallax-screen{
    height: 100vh !important;
  }
}
</style>
<style type="text/css">
.v-responsive__content{
  align-self: flex-end;
}
</style>

