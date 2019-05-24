<template>
  <v-container fluid pa-0 style="height: 50px">
    <v-layout mb-0 pa-0 row wrap justify-center>
        <!-- <v-tabs v-model="active" color="#00000000" dark slider-color="#136CE2" class="hidden-sm-and-down">
          <v-flex style="justify-content: flex-start;" justify-start xs1 class="v-tabs__div nav-info">
            <a class="hidden-xs nav-link" href="">8 800 550 39 34</a>
          </v-flex>
          <v-flex justify-end xs1 class="v-tabs__div nav-info text-lowercase">
            <a class="hidden-xs nav-link" href="">info@slv24.ru</a>
          </v-flex>
          <v-spacer></v-spacer>
          <v-flex xs1 v-for="nav in navLinks" :key="nav-link">
            <nuxt-link tag='p' style='margin-bottom: 0px; height: 100%;' :to="nav.link">
              <v-tab ripple class="text-capitalize">
                 {{ nav.name }}
              </v-tab>
            </nuxt-link>
          </v-flex>
            <v-tab-item style="width: 100%;" v-for="n in navLinks.length" :key="n"></v-tab-item>
          <v-spacer></v-spacer>
        </v-tabs> -->

        <v-flex offset-xs2 xs10>
          <v-tabs
          v-model="active"
          color="#00000000"
          dark
          slider-color="#136CE2"
          class="hidden-sm-and-down"
          >
          <v-flex class="v-tabs__div nav-info text-lowercase" xs2>
            
            <a style="margin: 0 5%" class="hidden-xs nav-link" href="">8 800 550 39 34</a>
            <a style="margin: 0 5%" class="hidden-xs nav-link" href="">info@slv24.ru</a>
          </v-flex>
          <v-flex class="v-tabs__div text-lowercase" offset-xs3 xs5>
            <nuxt-link
            class="nav-links"
            v-for="nav in navLinks"
            :key="n"
            :to="nav.link">
            <v-tab ripple class="text-capitalize"> {{ nav.name }} </v-tab>
          </nuxt-link>
          <v-tab-item
          v-for="n in 6"
          :key="n"
          >
        </v-tab-item> 
        <v-menu bottom left>
          <template v-slot:activator="{ on }">
            <v-tab v-on="on" ripple class="text-capitalize"> {{ currentLang }} <v-icon>expand_more</v-icon> </v-tab>
          </template> 
          <v-list dark>
            <v-list-tile
            v-for="lang in langs"
            :key="i"
            @click=""
            >
            <v-list-tile-title ripple class="text-capitalize">{{ lang.name }}</v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-menu>
    </v-flex>
  </v-tabs>
</v-flex>


<v-flex xs12>
  <v-card dark class="hidden-md-and-up" flat width="100vw">
    <v-card-title class="mobile-nav white--text">
      <div class="nav-info">
        <a style="margin-right: 10px;" class="nav-link" href="">
          8 800 550 39 34
        </a>
      </div>
      <div class="nav-info text-lowercase">
        <a class="nav-link" href="">
          info@slv24.ru
        </a>
      </div>
      <v-spacer></v-spacer>
      <v-menu bottom left>
        <template v-slot:activator="{ on }">
          <v-btn
          dark
          icon
          v-on="on"
          >
          <v-icon>menu</v-icon>
        </v-btn>
      </template>
      <v-list dark>
        <v-list-tile
        v-for="nav in navLinks"
        :key="i"
        :to="nav.link"
        @click=""
        >
        <v-list-tile-title ripple class="text-capitalize">{{ nav.name }}</v-list-tile-title>
      </v-list-tile>
    </v-list>
  </v-menu>
</v-card-title>
</v-card>
</v-flex>
</v-layout>
</v-container>
</template>

<script>
  export default {
    data () {
      return {
        active: null,
        items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' }
        ],
        on: true,
        navLinks:
        [
          {
            name: 'Главная',
            link: '/',
          },
          {
            name: 'Ассистент',
            link: '/',
          },
          {
            name: 'Тарифы',
            link: '/tarifs',
          },
          {
            name: 'Для Бизнеса',
            link: '/buisness',
          },
          {
            name: 'Контакты',
            link: '/contacts',
          },
          {
            name: 'Войти',
            link: '/signin',
          },
        ],
        langs: [
          {
            name: 'RUS',
            link: '/',
          },
          {
            name: 'CHA',
            link: '/',
          },
          {
            name: 'ENG',
            link: '/',
          },
        ],
        currentLang: 'RUS'
      }
    },
    mounted() {

    },
    methods: {
      next () {
        const active = parseInt(this.active)
        this.active = (active < 2 ? active + 1 : 0)
      }
    }
  }
</script>

<style lang="stylus" scoped>
.theme--dark.v-list 
  background: #000000a0;
.nav-links
  height 100%
  text-decoration none
  &:nth-child(4)
    min-width: 110px;
.layout
  background #000000a0
.nav-link
  color white
  text-decoration none
.theme--dark.v-sheet
  background none
.mobile-nav
  background #000000a0 !important
.v-tabs__div
  display: flex;
  height: 100%;
// .v-tabs__container
// 	margin: auto 5vw
// 	.v-tabs__div
// 		width 5vw
// 	.nav-info
// 		padding 12px 6px 
// 		width 10vw
// 	.v-tabs__div:nth-child(3)
// 		margin-right 38vw
// 	.v-tabs__div:nth-child(2)
// 		width 7vw
// 		margin-left 5vw
// 	.v-tabs__div:last-child
// 		margin-right 5vw
.nav-info
    margin auto none
</style>

<!-- <style scoped>

@media screen and (max-width: 1200px){
  
}
</style> -->
