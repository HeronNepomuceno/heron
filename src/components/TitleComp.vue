<template>
	<div class="title-wrapper">
		<h3 class="title" v-bind:class="{ color_blue: color_blue_status, color_white: color_white_status}" >{{ title }}</h3>
	</div>
</template>

<script>
export default {
	name: 'TitleComp',
	props: {
		title: String,
		color_blue_status: Boolean,
		color_white_status: Boolean
	}
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.color_blue
	color var(--darkBlueColor)
	text-decoration underline var(--darkBlueColor)
	
.color_white
	color var(--onDarkBlueColor)
	text-decoration underline var(--onDarkBlueColor)

.title-wrapper
	align-items center
	display flex
	justify-content center
	padding-bottom 32px
	width 100%

.title
	font-family var(--fontPrimary)
	font-size 28px

	@media (min-width: 600px)
		font-size 36px

	@media (min-width: 840px)
		font-size 42px
</style>>