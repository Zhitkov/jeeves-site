<template>
  <v-layout class="full-screen" row wrap>
    <v-flex xs2>
      
      <v-img class="parallax-screen change" dark :lazy-src="require('../../static/tarifs/preview.png')" cover :src="require('../../static/tarifs/preview.png')" gradient="to top right, rgba(1, 22, 46, 0.2), rgba(1, 22, 46, 0.2)">
      <v-flex offset-xs2>
        <img class="logo2" style="padding-bottom: 42px;" :src="logo">
      </v-flex>
    </v-img>
    </v-flex>
  </v-layout>
</template>

<script>

  export default {
    components: {

    },
    data () {
      return {
        logo: require('../../static/logos/logo2.svg'),
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
  width 100vwz
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
.logo2{

}
@media screen and (max-width: 1400px){

}
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
<style type="text/css">
.v-responsive__content{
  align-self: flex-end;
}
</style>

