<template>
	<v-container pa-0 :style="'background-image: url(' + bg + ')'" fluid>
		<v-layout row wrap class="hei100">
			<v-flex md6 xs12 class="fourth-container hei100">
				<img :src="logo">
				<h1>Мобильное приложение</h1>
				<div class="phone-container">
					<p>Введите номер телефона, чтобы получить ссылку на приложение </p>
					<div style="display: flex">
						<PhoneForm/>
						<v-btn large color="primary">Отправить заявку</v-btn>
					</div>
				</div>
					<appInstallButtons class="fourth-app-install"/>
			</v-flex>
			<v-flex md5 xs12 class="hei100">
				<v-img
					cover
                  :src="phone"
                  :lazy-src="phone"
                  position="center 20%"
                >
            </v-img>
			</v-flex>
		</v-layout>
	</v-container>
</template>
<script>
import appInstallButtons from '~/components/layouts/appInstallButtons.vue'
import PhoneForm from '~/components/layouts/PhoneForm.vue'

export default {
	components: {
      appInstallButtons,
      PhoneForm,
    },
	data () {
		return {
			bg: require('../../static/Fourth/bg.png'),
			phone: require('../../static/Fourth/iphone.png'),
			logo: require('../../static/Fourth/logo2.png'),
		}
	}
}
	
</script>
<style lang="css" scoped>
	.hei100, .v-image{
	    height: 100% !important;
	}
	.container{
		background-size: cover;
		width: 100vw;
		height: 70vh;
		color: white;
	}
	.fourth-container{
		margin: 2% 4%;
	}
	.phone-container{
		display: flex;
		-webkit-flex-direction: column;
		    -ms-flex-direction: column;
		        flex-direction: column;
		margin: 10% 0% 0%;
	}
	.fourth-app-install{
		text-align: left;
	}
	.v-btn{
	    margin: 2px 10px;
	}
</style>
<style scoped>
@media screen and (max-width: 900px){
	.container{
		height: 85vh;
	    padding: 20px !important;
    }
    .v-btn--large {
	    font-size: 15px;
	    height: 44px;
	    padding: 0 16px;
	}
	.fourth-app-install{
		text-align: center !important;
	}
	.v-image{
		display: none !important;
	}
	.phone-container > div{
		display: flex;
	    flex-direction: column;
	    align-items: center;
	    padding-bottom: 10px;
	}
	.downloads{
	    text-align: center !important;
	}
}
</style>