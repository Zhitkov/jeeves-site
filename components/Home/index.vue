<template>
  <v-container ma-0 pa-0 style="min-width: 100vw">
    <v-layout
    column
    justify-center
    align-center
    >
      <v-flex xs12>
        <TheFirst />
      </v-flex>
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
</v-container>
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
