<template>
	<v-container fluid>
		<v-layout style="justify-content: center" row wrap>
			<v-flex xs11>
				<h1 style="width: 60%" class="second-title">Наши водители — профессионалы, соблюдающие этикет и корпоративные стандарты в выполнении своих обязанностей, в поведении и внешнем виде.</h1>
					<div md6 xs12 class="second-list">
						<ul>
							<li>Тщательный отбор в соответствии со строгими критериями.</li>
							<li>Классический костюм и галстук.</li>
							<li>Владеют иностранными языками.</li>
							<li>Подождут в аэропорту с табличкой, если укажете номер рейса.</li>
							<li>Откроют для Вас дверь, помогут с багажом, в случае дождя встретят с зонтом. </li>
							<li>Прислушиваются к Вашим пожеланиям по маршруту, музыке, температуре.</li>
						</ul>
					</div>

			</v-flex>
		</v-layout>
	</v-container>
</template>
<style lang="stylus" scoped>
.container 
	background-image url('../../static/Second.png')
	background-size cover
	background-color #000 
	margin 0
	width 100vw !important
	padding 0 5vw
	height auto
	.second-title
		color white
	    font-size 10.5px 
	.second-list
		ul
			margin 2% 0
			li
				color white
				font-size 16px
				margin-top 5px
.flex
	    margin 3vw 0
</style>
<style scoped>
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