<template>
  <v-layout class="full-screen" row wrap>
    <v-spacer></v-spacer>
    <v-flex xs12>
    <v-parallax v-loading="completeNext﻿" class="parallax-screen change" dark :lazy-src="bg" :src="bg">
          <v-flex offset-md2 md2 offset-xs3 xs6 style="min-width: 212px;">
            <Logo class="opa" style="display: flex;justify-content: flex-start;     align-items: center;"/>
          </v-flex>
    </v-parallax>
    <v-flex offset-md2 md8 offset-xs1 xs10>
      <h1 class="First-text">Комфорт поездок бизнес-классом и личный ассистент в одном мобильном приложении </h1>
      <Border style="margin-left: 0;width: 100%"/>
      <h1 class=" neue First-text">Установить</h1>
      <appInstallButtons/>
    </v-flex>
  </v-flex>
    <v-spacer></v-spacer>
  </v-layout>
</template>

<script>
import Logo from '~/components/layouts/Logo.vue'
import Border from '~/components/layouts/Border.vue'
import appInstallButtons from '~/components/layouts/appInstallButtons.vue'
  export default {
    components: {
      Logo,
      Border,
      appInstallButtons
    },
    data () {
      return {
        bg: require('../../static/Home/First.png')
      
    }
  }
    // methods: {
    //   completeNext﻿: function () {
    //   var tl = new TimelineMax;
    //   tl.add(
    //         TweenLite.to('.opa', 1, {opacity: 1}),
    //       );
    // },
  // }
}
</script>

<style lang="stylus" scoped>
.neue
  font-size: 36px;
  line-height: 36px; 
.full-screen
  width 100vw
.parallax-screen
  width 100vw
  height 76vh !important
  .v-parallax__content > .container
    align-content: center;
    align-items: center;
    align-self: center;
    display: flex;
    .opa 
      opacity 1
.First-text
  text-align center 
  font-size 32px
  margin 50px 0 10px
  font-weight 500
  &:nth-child(3)
    margin 2% 25% 1%
.downloads
  margin-bottom 10vw 
</style>
<style scoped>
@media screen and (max-width: 900px){
  .First-text{
    font-size: 20px; 
    margin: 5% 10% 1%;
  }
  .parallax-screen{
    height: 100vh !important;
  }
}
</style>


