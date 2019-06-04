<template>
		<v-flex xs12 style="height: 55vh;">
	<v-img cover :src="bg" style="width: 100vw; max-height:70vh">
			<v-layout style="display: flex; justify-content: center;" row wrap>
				<div class="static">
				<v-flex px-2 mx-4 md6 xs12 class="fourth-block">
					<img :src="logo">
					<h1 class="neue">Мобильное приложение</h1>
					<div class="phone-container">
						<p>Введите номер телефона, чтобы получить ссылку на приложение </p>
						<div style="display: flex">
							<PhoneForm/>
							<v-btn large color="primary">Отправить заявку</v-btn>
						</div>
					</div>
					<appInstallButtons class="fourth-app-install"/>
				</v-flex>
				<v-flex  xs6 class="fourth-phone">
					<v-img
					xs5
					contain
					:src="phone"
					:lazy-src="phone"
					position="120% 10%"
					>
				</v-img>
			</v-flex>
			</div>
		</v-layout>
</v-img>
	</v-flex>
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
			phone: require('../../static/Home/Fourth/iphone.webp'),
			logo: require('../../static/logos/logo2.svg'),
		    bg: require('../../static/Home/Fourth/bg.webp'),
		}
	}
}
	
</script>
<style lang="css" scoped>
	.neue {
	  font-size: 36px;
	  line-height: 36px; 
	  font-weight: 100;
	  color: white;
  	}
	.fourth-block {
		margin-top: 45px;
	}
	.phone-container {
		font-weight: 300;
		display: flex;
		-webkit-flex-direction: column;
		    -ms-flex-direction: column;
		        flex-direction: column;
		margin: 10% 0% 0%;
	}
	.phone-container > p {
		color: #FFF;
	}
	.fourth-app-install {
		text-align: left;
	}
	.v-btn {
	    margin: 2px 10px;
	}
</style>
<style scoped>

@media screen and (max-width: 1400px){
.fourth-container {
		margin-top: 45px;
	}
}
@media screen and (max-width: 900px){
	.fourth-container {
		margin-top: 45px;
	    padding-left: 0;
	}
	.container{
		max-height: 80vh;
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
	.fourth-phone {
		display: none;
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
.v-responsive__content {
	    height: 55vh;
}
</style>
<style type="text/css">
div[data-v-32a09d94] .v-responsive__content{
	    align-self: center;
}
div[data-v-32a09d94] .v-responsive.v-image{
	    height: 55vh;
}
</style>