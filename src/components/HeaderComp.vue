<template>
	<header class="header">
		<div class="img-wrapper">
			<img src="/images/clouds.svg" alt="Night Sky">
		</div>
		<div class="banner">
			<h1 class="title">Heron Nepomuceno</h1>
			<h2 class="subtitle">Desenvolvedor Frontend</h2>
			<h3 class="subtitle">Designer UI/UX</h3>
			<div class="button-wrapper">
				<button class="button" @click="scrollToPresentation">
					<svg class="icon">
						<use xlink:href="/images/icons/sprite.svg#white-balance-sunny"></use>
					</svg>
					<span class="text">Saiba mais</span>
				</button>
			</div>
		</div>
		<menu-comp/>
	</header>
</template>

<script>
import MenuComp from './MenuComp.vue'
export default {
	name: 'HeaderComp',
	components: { MenuComp },
	methods: {
		scrollToPresentation() {
			setTimeout(() => {
				document.querySelector('#apresentacao').scrollIntoView();
			}, "1000")
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.header
	height 100vh
	width 100%
	overflow hidden
	position relative
	z-index 1

.img-wrapper
	height 100%
	width 100%
	overflow hidden
	position relative

	img
		height 100%
		width 100%
		object-fit cover

.banner
	align-items center
	background rgba(0, 0, 0, 0.5)
	border-radius 16px
	display flex
	flex-direction column
	left 50%
	top 32%
	padding 32px 16px
	position absolute
	width 320px
	transform: translate(-50%, -50%);
	z-index 2

	@media (min-width: 600px)
		width 520px
	
	@media (min-width: 840px)
		top 180px

.title
	font-family var(--fontPrimary)
	font-size 28px
	margin-bottom 32px
	text-decoration underline var(--onBlackColor)

	@media (min-width: 600px)
		font-size 36px

.subtitle
	font-family var(--fontSecondary)
	font-size 18px

	@media (min-width: 600px)
		font-size 26px

.button-wrapper
	display flex
	justify-content center
	width 100%

.button
	align-items center
	background var(--onDarkBlueColor)
	border-radius 16px
	color var(--darkBlueColor)
	display flex
	font-family var(--fontSecondary)
	margin-top 48px
	padding 8px 32px
	transition background .3s

	&:focus
		background var(--onBlackColor)

	&:focus .icon
		transform rotate(180deg)

.icon
	fill currentcolor
	height 24px
	margin-right 8px
	width 24px
	transition transform 1s

	@media (min-width: 600px)
		height 32px
		margin-right 16px
		width 32px

.text
	font-size 16px

	@media (min-width: 600px)
		font-size 20px
</style>
