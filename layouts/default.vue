<template>
  <v-app light>
<!--     <v-container v-if="false" class="loading-container" fill-height fluid>
      <v-layout row justify-center align-center>
        <v-progress-circular indeterminate :size="70" :width="7" color="white"></v-progress-circular>
      </v-layout>
    </v-container> -->
    <div>
      <TheNavbar class="nav-fix"/>
        <nuxt />
      <TheFooter/>
    </div>
  </v-app>
</template>

<script>
import TheNavbar from '~/components/TheNavbar.vue'
import TheFooter from '~/components/TheFooter.vue'

export default {
  components:{
    TheNavbar,
    TheFooter,
  },
  data: () => ({
    loading: true
  }),
  mounted() {

  },
  methods: {
    look : () => {
      return this.loading = false;;
    }
  }
 
}
</script>

<style lang="stylus">
.static 
  justify-self: center;
  display: flex;
  align-self: center;
  max-width: 1200px !important;
  // width: 1200px !important;
@font-face {
    font-family: Neue;
    font-style: normal;
    src: url("../assets/fonts/9116.otf");
  }
.theme--light.application
  background: #fff !important
body
  overflow: hidden
  background: #fff
  .v-parallax__image
    min-height: 110vh;
  .loading-container
    background: #000000;
  .nav-fix
    position: fixed;
    z-index: 9999;
  .text-c
    text-align: center;
  .linkText
    text-decoration underline
    color #136CE2
    cursor pointer
  .neue
    font-family 'Neue' !important
@media screen and (max-width: 2000px) {
  .v-parallax__image{
    min-height: 137vh !important;
  }
}

div[data-v-5404b582] .v-text-field--outline > .v-input__control > .v-input__slot
  background: #fff !important;

div[data-v-5404b582] .v-text-field--outline.v-input--has-state>.v-input__control>.v-input__slot 
    background: white !important;
    
div[data-v-5404b582] .v-text-field--outline.v-input--is-focused>.v-input__control>.v-input__slot
    background: white !important;
    
div[data-v-2980cee7] .v-text-field--outline.v-input--is-focused>.v-input__control>.v-input__slot 
    background: white !important;
</style>