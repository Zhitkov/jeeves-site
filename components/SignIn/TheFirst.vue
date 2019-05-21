<template>
		<v-layout style="padding-top: 20vh; width: 100vw; height: 80vh; background: linear-gradient(to top, #000 0%, #ffffff50 100%) !important;" row wrap>
		  <v-flex offset-xs1 xs10 offset-md2 md4 justify-center>
		    <Logo/>
		  </v-flex>
		  <v-flex offset-xs1 xs10 offset-md1 md3>
		    <p class="title">Вход в личный кабинет</p>
		    <Form :aboutBuisness="false"/>
		  </v-flex>
		</v-layout>
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
			bg: require('../../static/Home/First.png'),
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
    justify-content: center;
}
</style>
<style>
	.v-parallax__content {
	padding: 0 !important;
}
</style>
