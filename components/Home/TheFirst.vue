<template>
  <v-layout class="full-screen" row wrap>
    <v-parallax v-loading="completeNext﻿" class="parallax-screen change" dark :lazy-src="require('../../static/Uxar1First.png')" :src="require('../../static/Uxar1First.png')">
      <v-container>
        <v-layout row wrap>
          <v-flex xs12 md6>
            <Logo class="opa"/>
          </v-flex>
        </v-layout>
      </v-container>
    </v-parallax>
    <v-flex style="background: white" xs12>
      <h1 class="First-text">Комфорт поездок бизнес-классом и личный ассистент в одном мобильном приложении </h1>
      <Border style="width: 100vw;"/>
      <h1 class=" neue First-text">Установить</h1>
      <appInstallButtons/>
    </v-flex>
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
.neue
  font-size: 36px;
  line-height: 36px; 
.full-screen
  width 100vw
.parallax-screen
  width 100vw
  height 80vh !important
  .v-parallax__content > .container
    align-content: center;
    align-items: center;
    align-self: center;
    display: flex;
    .opa 
      opacity 1
.First-text
  text-align center 
  font-size 1.6vw 
  margin 5% 25% 1%
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

