<template>
	<div class="phone-form">
		 <v-select
          :items="items"
          label="+7"
          solo
          background-color="#333333"
          dark
          style="width: 30% !important;"
        ></v-select>
        <v-text-field
        	class='tel-mask'
            label="Телефон"
            single-line
            solo
            mask="(###) ###-##-##"
            dark
            required
          ></v-text-field>
	</div>
</template>

<script>
 export default {
    data: () => ({
      items: ['+7', '+1', '+12'],
    })
  }
</script>

<style lang="css" scoped>
	.phone-form{
		display: flex;
		-webkit-flex-wrap: nowrap;
		-ms-flex-wrap: nowrap;
		flex-wrap: nowrap;
		-webkit-flex-direction: row;
		    -ms-flex-direction: row;
		        flex-direction: row;
		width:  250px;
		align-content: center;
	}
</style>

<style lang="stylus">
  .v-input__slot
    min-width 60px
	.tel-mask .v-input__slot
		background linear-gradient(90deg, #393185 0%, #18F2D9 100%) !important
</style>