<template>
<section id="portfolio" class="portfolio">
	<title-comp title="Currículo" :color_blue_status="true"/>
	<div class="info-wrapper">
		<span class="info-text">Para baixar o currículo do programador, clique no botão abaixo!</span>
		<a class="info-download" href="HeronNepomuceno-CV.pdf" download>
			<span class="info-button-text">Baixar em pdf</span>
			<svg class="info-icon">
				<use xlink:href="/images/icons/sprite.svg#pdf"></use>
			</svg>
		</a>
	</div>
</section>
	
</template>

<script>
import TitleComp from './TitleComp.vue'
export default {
	name: "PortfolioComp",
	components: { TitleComp }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.portfolio
	align-items center
	background var(--onDarkBlueColor)
	display flex
	flex-direction column
	justify-content center
	padding 48px 32px 80px 32px
	width calc(100% - 64px)

.info-wrapper
	align-items center
	display flex
	flex-direction column
	font-family var(--fontSecondary)
	justify-content center

.info-text
	color var(--darkBlueColor)
	font-size 16px
	margin-bottom 32px
	text-align center

	@media (min-width 600px)
		font-size 24px
		margin-right 16px

	@media (min-width 840px)
		font-size 36px

	&::first-letter
		font-size 36px

		@media (min-width: 840px)
			font-size 80px

.info-download
	align-items center
	background var(--darkBlueColor)
	color var(--onDarkBlueColor)
	border-radius 16px
	display flex
	justify-content center
	padding 16px 24px
	transition opacity .3s

	&:hover
		opacity .8

.info-button-text
	margin-right 8px

	@media (min-width: 600px)
		margin-right 16px
		font-size 20px

.info-icon
	fill currentcolor
	height 24px
	width 24px

	@media (min-width: 600px)
		height 32px
		width 32px

</style>