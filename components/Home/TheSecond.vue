<template>
	<v-img class="second-block"  style="min-width: 100vw; width: auto;" :lazy-src="bg" :src="bg" fluid>
		<v-layout style="justify-content: center" row wrap>
			<v-flex xs8 style="margin: 20px 0 0 105px">
				<v-flex offset-xs1 xs6 style="margin: 0 0 30px 0; min-width: 430px;">
					<h1 class="second-title">Наши водители — профессионалы, соблюдающие этикет и корпоративные стандарты в выполнении своих обязанностей, в поведении и внешнем виде.</h1>
				</v-flex>
				<ul class="second-list">
					<li>Тщательный отбор в соответствии со строгими критериями.</li>
					<li>Классический костюм и галстук.</li>
					<li>Владеют иностранными языками.</li>
					<li>Подождут в аэропорту с табличкой, если укажете номер рейса.</li>
					<li>Откроют для Вас дверь, помогут с багажом, в случае дождя встретят с зонтом. </li>
					<li>Прислушиваются к Вашим пожеланиям по маршруту, музыке, температуре.</li>
				</ul>

			</v-flex>
		</v-layout>
	</v-img>
</template>
<script type="text/javascript">
	export default {
		data() {
			return {
				bg: require('../../static/Home/Second.png')
			}
		}
	}
</script>
<style lang="stylus" scoped>
.container 
	background-size cover
	background-color #000 
	margin 0
	width 100vw !important
	padding 0 5vw
	height auto
.flex
	    margin 3vw 0
</style>
<style scoped>
.second-title{
	color: white;
    font-size: 21px; 
	margin: 10px auto;
}
.second-list{
	margin: 10px 10px 10px 0px;
}
.second-list > li{
	color: white;
	font-size: 16px;
	margin: 10px auto;
}

@media screen and (max-width: 900px){
	.container {
		background-image: none;
	}
	.second-title{
		font-size: 18px;
	}
	.second-list > ul > li {
		font-size: 16px !important;
	}
	
}
</style>
<style type="text/css">
.second-block .v-responsive__content {
	align-self: center !important;
}
</style>