<template>
	<v-parallax style="width: 100vw;" :src="require('../../static/Second.png')" fluid>
		<v-layout style="justify-content: center" row wrap>
			<v-flex offset-xs2 xs8>
				<h1 class="second-title">Наши водители — профессионалы, соблюдающие этикет и корпоративные стандарты в выполнении своих обязанностей, в поведении и внешнем виде.</h1>
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
	</v-parallax>
</template>
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
	margin: 10px;
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