<template>
  <div class="item-project">
    <div class="head">
      <span>{{ project_name }}</span>

			<div class="focus-within" tabindex="0">
				<button class="icon-button focus-button-1" aria-label="Informações do projeto">
					<svg class="icon icon--short">
						<use xlink:href="/images/icons/sprite.svg#information-outline"></use>
					</svg>
				</button>
				<div class="info">
					{{ project_info }}
				</div>
			</div>
			<button class="icon-button focus-button-2" aria-label="Informações do projeto">
				<svg class="icon icon--short">
					<use xlink:href="/images/icons/sprite.svg#information-outline"></use>
				</svg>
			</button>
    </div>
    <div class="body">
      <img class="image" :src="(`/images/project/${project_image}`)" alt="Project Image">
    </div>
    <div class="footer">
      <a class="icon-button" :href="project_github" target="_blank" aria-label="Acessar github do projeto">
        <svg class="icon">
          <use xlink:href="/images/icons/sprite.svg#github"></use>
        </svg>
      </a>
      <a class="icon-text-button" :href="project_link" target="_blank">
        <span class="text">Acessar projeto</span>
        <svg class="icon">
          <use xlink:href="/images/icons/sprite.svg#subdirectory-arrow-right"></use>
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItemProjectComp',
	props: {
		project_name: String,
		project_image: String,
		project_info: String,
		project_link: String,
		project_github: String,
	}
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'
  
.item-project
	align-items center
	background var(--onDarkBlueColor)
	border-top-left-radius 8px
	border-top-right-radius 8px
	color var(--darkBlueColor)
	display flex
	flex-direction column
	font-family var(--fontSecondary)
	margin-top 32px
	padding 16px 16px 0 16px
	position relative
	width 280px

	@media(min-width 600px)
		width 300px

.head
	align-items center
	display flex
	font-family var(--fontPrimary)
	font-size 20px
	justify-content space-between
	margin-bottom 32px
	width 100%

.focus-within
	&:focus-within .focus-button-1
		height 0
		width 0
	&:focus-within ~ .focus-button-2
		display flex
	&:focus-within .info
		opacity 1
		visibility visible

.info
	background var(--onBlackColor)
	border-radius 8px 0 8px 8px
	border 1px solid var(--blackColor)
	box-shadow 0 2px 5px 0 rgba(11, 20, 26, .26),0 2px 10px 0 rgba(11, 20, 26, .16)
	font-family var(--fontSecondary)
	font-size 16px
	left 16px
	opacity 0
	padding 8px 16px
	position absolute
	right 32px
	top 42px
	visibility hidden

.body
	align-items center
	display flex
	flex-direction column
	width 100%

.image
	background rgba(0, 0, 0, 0.3)
	height 140px
	padding 16px
	width 100%

.footer
	align-items center
	border-bottom 8px solid var(--blackColor)
	display flex
	justify-content space-between
	margin-top 32px
	padding 16px
	width 100%

.icon-button
	align-items center
	background var(--darkBlueColor)
	border-radius 32px
	color var(--onDarkBlueColor)
	display flex
	justify-content center
	transition opacity .3s

	.icon
		fill currentcolor
		height 32px
		width 32px

		&--short
			height 24px
			width 24px

	&:hover
		opacity .8

.focus-button-2
	display none

.icon-text-button
	align-items center
	border 1px solid var(--darkBlueColor)
	border-radius 16px
	color var(--darkBlueColor)
	display flex
	justify-content center
	padding 4px 16px
	transition opacity .3s

	.text
		font-size 16px
		margin-right 8px

	.icon
		fill currentcolor
		height 16px
		width 16px
	
	&:hover
		opacity .8

</style>