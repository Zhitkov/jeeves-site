<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex  xs12>
        <TheFirst />
    </v-flex>
    <v-flex xs12>
        <TheSecond />
      </v-flex>
      <!-- <v-flex xs12>
        <TheThird />
      </v-flex>
      <v-flex xs12>
        <TheFourth />
      </v-flex> -->
  </v-layout>
</template>

<script>
import TheFirst from '~/components/Tarifs/TheFirst.vue'
import TheSecond from '~/components/Tarifs/TheSecond.vue'
// import TheThird from '~/components/Tarifs/TheThird.vue'
// import TheFourth from '~/components/Tarifs/TheFourth.vue'

export default {
  components: {
    TheFirst,
    TheSecond,
    // TheThird,
    // TheFourth,
  }
}
</script>
