<template>
	<footer class="footer">
		<h5 class="copyright">© {{ current_year }} Heron Nepomuceno</h5>
		<div class="social">

			<a class="link" aria-label="Visite meu Linkedin" href="https://www.linkedin.com/in/heron-nepomuceno-b3125b1b6" target="_blank">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#linkedin"></use>
				</svg>
			</a>
			<a class="link" aria-label="Visite meu Github" href="https://github.com/HeronNepomuceno" target="_blank">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#github"></use>
				</svg>
			</a>
		</div>
	</footer>
</template>

<script>
export default {
	name: "FooterComp",
	data: function() {
		return {
			current_year: ''
		}
	},
	mounted() {
		let date =  new Date().getFullYear()
		this.current_year = date
	}
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'
.footer
	align-items center
	display flex
	flex-direction column
	padding 32px
	width calc(100% - 64px)

	@media (min-width 840px)
		padding 48px
		width calc(100% - 96px)

.copyright
	font-family var(--fontSecondary)
	font-size 18px

	@media (min-width 600px)
		font-size 22px

	@media (min-width 840px)
		font-size 26px

.social
	align-items center
	display flex
	margin-top 32px

.link
	transition transform .3s

	&:hover
		transform scale(1.1)

.icon
	fill var(--onDarkBlueColor)
	height 32px
	margin 0 8px
	width 32px

	@media (min-width 600px)
		height 48px
		width 48px
</style>