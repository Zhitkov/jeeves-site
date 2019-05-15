<template>
  <div>
    <v-tabs
      v-model="active"
      color="#000000a0"
      dark
      slider-color="#136CE2"
      class="hidden-sm-and-down"
    >
    <div class="v-tabs__div nav-info">
    	<a class="hidden-sm-and-up nav-link" href=""><v-btn dark icon v-on="on"><v-icon>phone_iphone</v-icon></v-btn></a>
      <a class="hidden-xs nav-link" href="">8 800 550 39 34</a>
    </div>
    <div class="v-tabs__div nav-info text-lowercase">
    	<a class="hidden-sm-and-up nav-link" href=""><v-btn dark icon v-on="on"><v-icon>email</v-icon></v-btn></a>
      <a class="hidden-xs nav-link" href="">info@slv24.ru</a>
    </div>
      <v-tab
        v-for="n in 7"
        :key="n"
        ripple
        class="text-capitalize"
      >
        <nuxt-link to="/tarifs"> tarifs </nuxt-link>

      </v-tab>
      <v-tab-item
        v-for="n in 7"
        :key="n"
      >
      </v-tab-item>
    </v-tabs>
      <v-card dark class="hidden-md-and-up" flat width="100vw">
        <v-card-title class="mobile-nav white--text">
          <div class="nav-info">
              <a class="nav-link" href="">
                <!-- <v-btn dark icon v-on="on"><v-icon>phone_iphone</v-icon></v-btn> -->
                8 800 550 39 34
              </a>
            </div>
            <div class="nav-info text-lowercase">
                <a class="nav-link" href="">
                <!-- <v-btn dark icon v-on="on"><v-icon>email</v-icon></v-btn> -->
                info@slv24.ru</a>
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
                v-for="(item, i) in items"
                :key="i"
                @click=""
              >
                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
              </v-list-tile>
            </v-list>
          </v-menu>
        </v-card-title>
      </v-card>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        active: null,
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
        items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' }
      ],
      on: true
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
  background #000000a0
.nav-link
  color white
  text-decoration none
.theme--dark.v-sheet
  background: none;
.mobile-nav
  background #000000a0 !important
.v-tabs__container
	margin: auto 5vw
	.v-tabs__div
		width 5vw
	.nav-info
		padding 12px 6px 
		width 10vw
	.v-tabs__div:nth-child(3)
		margin-right 38vw
	.v-tabs__div:nth-child(2)
		width 7vw
		margin-left 5vw
	.v-tabs__div:last-child
		margin-right 5vw
</style>

<style scoped>
@media screen and (max-width: 1520px){
  .v-tabs__div:nth-child(3){
    margin-right: 15vw !important;
  }
  .v-tabs__div{
    width: 8vw !important;
  }
  .nav-info{
    width: 12vw !important;
  }
}
@media screen and (max-width: 960px){
  .nav-info:first-child{
    padding: 0 0 0 20px;
  }
  .mobile-nav{
    padding: 15px 0px !important;
  }
  .menuable__content__active{
    top: 80px !important;
  }
  .nav-info{
      width: 45% !important;
  }
  .v-btn.v-btn--icon{
    width: 10vw;
    padding: 0 20px 0 0;
    margin: 0;
    max-width: 40px;
    padding-right: 1px;
  }
}
</style>
