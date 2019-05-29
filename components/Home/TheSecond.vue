<template>
			<v-layout row wrap>
	<v-img class="second-block" cover style="justify-content: center; width: 100vw;" :lazy-src="bg" :src="bg">
				<v-flex md12>
					<v-flex offset-xs1 xs10 offset-md2 md4>
						<h1 class="second-title">Наши водители — профессионалы, соблюдающие этикет и корпоративные стандарты в выполнении своих обязанностей, в поведении и внешнем виде.</h1>
					</v-flex>
					<v-flex offset-xs1 xs10 offset-md2 md6>
					<ul class="second-list">
						<li>Тщательный отбор в соответствии со строгими критериями.</li>
						<li>Классический костюм и галстук.</li>
						<li>Владеют иностранными языками.</li>
						<li>Подождут в аэропорту с табличкой, если укажете номер рейса.</li>
						<li>Откроют для Вас дверь, помогут с багажом, в случае дождя встретят с зонтом. </li>
						<li>Прислушиваются к Вашим пожеланиям по маршруту, музыке, температуре.</li>
					</ul>
					</v-flex>

				</v-flex>
	</v-img>
			</v-layout>
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
	margin 0
	width 100vw !important
	padding 0 5vw
	height auto
// .flex
// 	    margin 3vw 0
</style>
<style scoped>
.second-title{
	color: white;
    font-size: 21px; 
	margin: 10px auto;
	font-weight: 500
}
.second-list{
	margin: 10px 10px 10px 0px;
	font-weight: 500
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
.layout.row.wrap[data-v-e67e62e0] .v-responsive__sizer {
	padding: 10% 0 !important;
}
</style>