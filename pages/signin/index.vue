<template>
  <v-parallax class="parallax-screen" cover :src="bg" :lazy-src="bg">
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex xs12>
        <TheFirst />
    </v-flex>
  </v-layout>
  </v-parallax>
</template>

<script>
import TheFirst from '~/components/SignIn/TheFirst.vue'

export default {
  components: {
    TheFirst,
  },
  data () {
    return {
      bg: require('../../static/Home/First.png'),
    }
  }
}
</script>
<style scoped>
  .parallax-screen{
  width: 100vw;
  height: 80vh !important;
}
</style>