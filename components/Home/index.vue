<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-parallax v-loading="completeNext﻿" class="parallax-screen change" dark :lazy-src="bg1" :src="bg1">
      <v-flex xs12 style="display: flex">
          <TheFirst />
      </v-flex>
    </v-parallax>
    <v-container>
      <v-layout row wrap>
        <v-flex offset-md2 md8 xs12>
          <h1 class="First-text">Комфорт поездок бизнес-классом и личный ассистент в одном мобильном приложении </h1>
          <Border/>
          <h1 class=" neue First-text" style="font-weight: 100;">Установить</h1>
          <appInstallButtons/>
        </v-flex>
      </v-layout>
    </v-container>
    <v-flex xs12>
        <TheSecond />
      </v-flex>
      <v-flex xs12>
        <TheThird />
      </v-flex>
        <v-flex xs12>
          <TheFourth />
        </v-flex>
  </v-layout>
</template>

<script>
import TheFirst from '~/components/Home/TheFirst.vue'
import TheSecond from '~/components/Home/TheSecond.vue'
import TheThird from '~/components/Home/TheThird.vue'
import TheFourth from '~/components/Home/TheFourth.vue'
import appInstallButtons from '~/components/layouts/appInstallButtons.vue'

export default {
  components: {
    TheFirst,
    TheSecond,
    TheThird,
    TheFourth,
    appInstallButtons
  },
  data () {
    return {
      bg1: require('../../static/Home/First.png'),
    }
  }

}
</script>

<style scoped>
  .v-image{
    width: 100%;
  }
  .parallax-screen{
    width: 100vw;
    height: 80vh !important;
  }
  .First-text{
    text-align: center;
    font-size: 32px;
    margin: 70px 0 30px;
  }
  .First-text:nth-child(3){
    /*margin: 2% 25% 1%;*/
  }
.downloads {
  margin-bottom: 10vw; 
}
</style>
