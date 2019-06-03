<template>
	<v-layout row wrap>
		<v-flex v-if="aboutBuisness">
				<v-flex xs12 >
					<v-text-field
					class="form-white"
					label="ФИО"
					outline
					></v-text-field>
				</v-flex>
			<v-flex xs12 >
				<v-text-field
				class="form-white"
				outline
				v-model="email"
				:rules="[rules.required, rules.email]"
				label="E-mail"
				></v-text-field>
			</v-flex>
			<v-flex xs12>
				<v-flex xs12>
					<v-text-field
					class="form-white"
					label="Компания"
					outline
					></v-text-field>
				</v-flex>
			</v-flex>
			<v-flex xs12 style="display: flex; flex-direction: row; flex-wrap: nowrap; justify-content: center;">
				<PhoneForm :aboutBuisness="true"/>
				<v-btn style="border-radius: 10px; margin-top: 0px; width: 50%; height: 50px;" color="primary" large>Отправить заявку</v-btn>
			</v-flex>
		</v-flex>
		<v-flex v-else xs12>
			<v-flex xs12>
				<v-flex xs12 >
					<v-text-field
					label="Логин"
					outline
					></v-text-field>
				</v-flex>
			</v-flex>
			<v-flex xs12>
				<v-flex xs12 >
					<v-text-field
						outline
			            v-model="password"
			            :append-icon="show1 ? 'visibility' : 'visibility_off'"
			            :rules="[rules.required, rules.min]"
			            :type="show1 ? 'text' : 'password'"
			            label="Пароль"
			            hint="At least 8 characters"
			            @click:append="show1 = !show1"
		          ></v-text-field>
				</v-flex>
			</v-flex>
			<v-flex xs12 justify-center style="flex-direction: column; display: flex; text-align: center;align-items: center;">
				<v-btn style="width: 50%;" color="primary" large>Войти</v-btn>
				<a class="remind-pass">Забыли пароль?</a>
			</v-flex>
		</v-flex>
</v-layout>
</template>

<script>
	import PhoneForm from '~/components/layouts/PhoneForm.vue'

	export default {
		components: {
			PhoneForm,
		},
		data () {
			return {
				required: value => !!value || 'Required.',
				show1: false,
		        password: '',
				rules: {
					email: value => {
						const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
						return pattern.test(value) || 'Invalid e-mail.'
					},
					required: value => !!value || 'Required.',
		            min: v => v.length >= 8 || 'Min 8 characters',
				}
			}
		},
		props:['aboutBuisness']
	}
</script>
<style>
.v-text-field--outline > .v-input__control > .v-input__slot{
		background: #fff !important;
		border-radius: 10px;
	}
.v-text-field--outline.v-input--has-state>.v-input__control>.v-input__slot, .v-text-field--outline.v-input--is-focused>.v-input__control>.v-input__slot {
    border: 2px solid;
    transition: border .3s cubic-bezier(.25,.8,.5,1);
    background: white !important;
}
</style>
