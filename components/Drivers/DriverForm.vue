<template>
	<v-layout row wrap>
	  <v-flex offset-xs2 xs4>
	    <v-flex xs9 >
			<v-select
			class='driver-select'
	          :items="cities"
	          label="Город"
	          outline
	          background-color="#fff"
	        ></v-select>
		</v-flex>
	    <v-flex xs9 >
			<v-select
			class='driver-select'
	          :items="workers"
	          label="Желаемый тип рабочих"
	          outline
	          background-color="#fff"
	        ></v-select>
		</v-flex>
	    <v-flex xs9 >
			<v-text-field
			class="form-white"
			label="ФИО"
			outline
			></v-text-field>
		</v-flex>
	    <v-flex xs9 >
			<v-text-field
			class="form-white"
			outline
			v-model="email"
			:rules="[rules.required, rules.email]"
			label="E-mail"
			></v-text-field>
		</v-flex>
	    <v-flex xs9 style="display: flex;">
			<PhoneForm class="driver-phone" :aboutBuisness="true" style="width: 50%;"/>
			<v-btn color="primary" large style="width: 50% !important; margin-top: 2px; border-radius: 3px;">Отправить заявку</v-btn>
		</v-flex>
	  </v-flex>
	  <v-flex column xs4>
    	<v-flex class="step" xs1 >
			<p class="step-title"> Заявка на сайте </p>
			<v-text-field
			class="form-white"
			label="1"
			outline
			disabled
			></v-text-field>
		</v-flex>
		<v-flex class="step" xs1 >
			<p class="step-title"> Собеседование </p>
			<v-text-field
			class="form-white"
			label="2"
			outline
			disabled
			></v-text-field>
		</v-flex>
		<v-flex class="step" xs1 >
			<p class="step-title"> Тест на вождение и знание города </p>
			<v-text-field
			class="form-white"
			label="3"
			outline
			disabled
			></v-text-field>
		</v-flex>
		<v-flex class="step" xs1 >
			<p class="step-title"> Внутреннее обучение </p>
			<v-text-field
			class="form-white"
			label="4"
			outline
			disabled
			></v-text-field>
		</v-flex>
		<v-flex class="step" xs1 >
			<p class="step-title"> Вы в команде </p>
			<v-text-field
			class="form-white"
			label="5"
			outline
			disabled
			></v-text-field>
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
		data: () => ({
			workers: ['Курьер', 'Водитель'],
			cities: ['Москва', 'Санкт-Петербург'],
			rules: {
				email: value => {
					const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
					return pattern.test(value) || 'Invalid e-mail.'
				},
				required: value => !!value || 'Required.',
			}
		}),
			props:['aboutBuisness'],
	}
</script>

<style type="text/css">
.driver-select .v-input__slot{
	border-color: gray !important
}
	.step .v-input__slot label{
		color: #000 !important;
	}
	.step .v-input__slot{
		padding: 0 20px !important;
		border-radius: 3px !important;
	}
	.step-title{
		font-weight: 500;
		font-size: 20px;
		position: absolute;
		margin-left: 80px;
	    margin-top: 13px;
	}
	.driver-phone .v-input__slot {
		    border: 1px solid gray !important;
	}
</style>