<template>
  <v-layout class="full-screen" row wrap>
    <v-parallax v-loading="completeNext﻿" class="parallax-screen change" dark :lazy-src="require('../../static/tarifs/preview.png')" :src="require('../../static/tarifs/preview.png')">
      <v-container>
        <v-layout row wrap>
          <v-flex xs12 md6>
            <img style="padding-bottom: 65px;" :src="logo">
          </v-flex>
        </v-layout>
      </v-container>
    </v-parallax>
  </v-layout>
</template>

<script>

  export default {
    components: {

    },
    data () {
      return {
        logo: require('../../static/Fourth/logo2.png'),
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
.full-screen
  width 100vw
div[data-v-00bd8e1c].container
  align-items: flex-end !important
.parallax-screen
  width 100vw
  height 74vh !important
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

