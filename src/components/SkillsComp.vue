<template>
	<section id="habilidades" class="skills">
		<title-comp title="Habilidades" :color_white_status="true"/>
		<div class="items-tech-wrapper">
			<item-tech-comp tech_name="HTML5">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#html5-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="CSS3">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#css3-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="JAVASCRIPT">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#javascript-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="VUEJS">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#vuejs-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="STYLUS">
				<svg class="icon icon--background">
					<use xlink:href="/images/icons/sprite.svg#stylus-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="FIGMA">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#figma-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="GIT">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#git-tech"></use>
				</svg>
			</item-tech-comp>
			<item-tech-comp tech_name="GITHUB">
				<svg class="icon icon--background">
					<use xlink:href="/images/icons/sprite.svg#github-tech"></use>
				</svg>
			</item-tech-comp>
		</div>
	</section>
</template>

<script>
import TitleComp from './TitleComp.vue'
import ItemTechComp from './ItemTechComp.vue'
export default {
	name: 'SkillsComp',
	components: {
		TitleComp,
		ItemTechComp
	}
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.skills
	align-items center
	display flex
	flex-direction column
	height 100%
	padding 48px 32px
	width calc(100% - 64px)

	@media(min-width 840px)
		padding 84px 16px
		width calc(100% - 32px)

.items-tech-wrapper
	display grid
	grid-template-columns 144px 144px
	grid-gap 32px
	justify-content center
	margin-top 16px
	width 100%

	@media(min-width 600px)
		grid-gap 48px
		grid-template-columns 160px 160px 160px

	@media(min-width 840px)
		grid-template-columns 160px 160px 160px 160px

	@media(min-width 1020px)
		grid-gap 64px
		grid-template-columns 192px 192px 192px 192px

.icon
	height 128px
	width 128px

	&--background
		background var(--onDarkBlueColor)
		border-radius 16px

</style>