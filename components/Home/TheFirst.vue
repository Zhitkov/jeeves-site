<template>
  <v-container style="display: flex; align-items: center; margin-left: 0;">
    <v-layout class="full-screen" row wrap>
            <v-flex offset-md1 md2 offset-xs3 xs6>
              <Logo class="opa"/>
            </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Logo from '~/components/layouts/Logo.vue'
import Border from '~/components/layouts/Border.vue'

  export default {
    components: {
      Logo,
      Border,
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

  // .v-parallax__content > .container
  //   align-content: center;
  //   align-items: center;
  //   align-self: center;
  //   display: flex;
  .opa 
    justify-content: center;
    padding-left: 40px;
</style>
<style scoped>
@media screen and (max-width: 900px){
  .First-text{
    font-size: 17px; 
    margin: 5% 10% 1%;
  }
  .parallax-screen{
    height: 100vh !important;
  }
}
</style>

