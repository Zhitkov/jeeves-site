<template>
			<v-layout row wrap>
		<v-flex xs12 style="height: 65vh;">
					<v-flex style="display; position: absolute; z-index: 9;margin-top: -5px;width: 33%;margin: -5px 33%;">
						<img class="logo" :src="logo">
					</v-flex>
	<v-img cover :src="bg" style="width: 100vw; height: 100%">
				<v-flex xs12 class="fourth-block">
					<v-flex offset-xs1 xs10 offset-md2 md8>
						<h1 class="neue big">СКАЧАТЬ ПРИЛОЖЕНИЕ ПРЯМО СЕЙЧАС</h1>
					</v-flex>
					<v-flex offset-md4 md4 offset-xs1 xs10 >
						<p style="color: white; font-weight: 500; text-align: center;">Введите номер телефона, чтобы получить ссылку на приложение </p>
						<div style="display: flex; justify-content: center;">
							<PhoneForm :aboutBuisness="true"/>
							<v-btn large color="primary">Отправить заявку</v-btn>
						</div>
					</v-flex>
					<appInstallButtons class="fourth-app-install"/>
				</v-flex>
				<v-flex  xs4 class="fourth-phone">
					<v-img
					xs5
					cover
					:src="phone"
					:lazy-src="phone"
					position="center 20%"
					>
				</v-img>
			</v-flex>
</v-img>
	</v-flex>
		</v-layout>
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
			logo: require('../../static/logos/logo2bg.svg'),
		    bg: require('../../static/Assistent/bg2.png'),
		}
	}
}
	
</script>

<style type="text/css">
	.neue.big {
		font-size: 72px;
		line-height: 64px;
		color: white;
	    text-align: center;
	}
	img {
		height: 20%;
	}
	.fourth-block {
		margin-top: 12%;
	}
</style>