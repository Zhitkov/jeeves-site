<template>
	<v-parallax class="parallax-screen" cover :src="bg" :lazy-src="bg">
		<v-layout style="padding-top: 20vh; width: 100vw;" row wrap>
		  <v-flex offset-xs3 xs6 offset-md3 md2 justify-start>
		    <Logo/>
		  </v-flex>
		  <v-flex pl-5 offset-md1 md3 offset-xs1 xs10>
		    <p class="title">Вход в личный кабинет</p>
		    <Form class="signIn" :aboutBuisness="false"/>
		  </v-flex>
		</v-layout>
  </v-parallax>
</template>

<script>
import Form from '~/components/layouts/Form.vue'
import Logo from '~/components/layouts/Logo.vue'


export default {
	components: {
      Form,
      Logo
    },
	data () {
		return {
			bg: require('../../static/Signin/bg.png'),
		}
	}
}
	
</script>
<style scoped>
.title{
	font-size: 30px !important;
    text-align: center;
    margin-bottom: 20px;
}
.text{
	font-size: 18px;
	font-weight: 100
}
.logo{
	display: flex;
    justify-content: flex-start;
}
</style>
<style>
	.v-parallax__content {
	padding: 0 !important;
}
</style>
