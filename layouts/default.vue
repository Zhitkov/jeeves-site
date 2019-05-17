<template>
  <v-app light>
    <v-container v-if="false" class="loading-container" fill-height fluid>
      <v-layout row justify-center align-center>
        <v-progress-circular indeterminate :size="70" :width="7" color="white"></v-progress-circular>
      </v-layout>
    </v-container>
    <div v-else>
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
    // window.addEventListener("load", function(event) {
    //   console.log("All resources finished loading!");
    // });
  },
  methods: {
    look : () => {
      return this.loading = false;;
    }
  }
  // mounted () {
  //   this.$nextTick(() => {
  //     this.$nuxt.$loading.start();
  //     this.loading = false
  //     setTimeout(() => this.$nuxt.$loading.finish(), 1000)
  //   })
  // }
}
</script>

<style lang="stylus">
@font-face {
    font-family: Neue;
    font-style: normal;
    src: url("../assets/fonts/9116.otf");
  }
body
  overflow: hidden;
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
</style>