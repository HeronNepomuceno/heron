<template>
  <nav class="menu">
    <button class="icon-button" @click="toggleMenu" aria-label="Menu de Navegação">
				<svg class="icon">
					<use xlink:href="/images/icons/sprite.svg#menu"></use>
				</svg>
    </button>
    <ul class="menu-items">
      <li class="menu-item"><a href="#top">Início</a></li>
      <li class="menu-item"><a href="#apresentacao">Sobre mim</a></li>
      <li class="menu-item"><a href="#habilidades">Habilidades</a></li>
      <li class="menu-item"><a href="#projetos">Projetos</a></li>
      <li class="menu-item"><a href="#portfolio">Saiba mais</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "MenuComp",
  methods: {
    toggleMenu() {
      let menu_button = document.querySelector('.icon-button')
      let menu_items = document.querySelector('.menu-items')

      menu_button.classList.toggle('icon-button--show')
      menu_items.classList.toggle('menu-items--show')
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.menu
  align-items center
  display flex
  flex-direction column
  justify-content center

.icon-button
  align-items center
  background var(--blackColor)
  border 1px solid var(--onBlackColor)
  border-radius 5px
  color var(--onDarkBlueColor)
  display flex
  justify-content center
  padding 4px
  position fixed
  transition color .3s, right .5s
  top 32px
  right 16px
  z-index 4

  &:hover
    color var(--onBlackColor)
  
  &--show
    right 188px

.icon
  fill currentcolor
  height 32px
  width 32px


.menu-items
  align-items center
  background var(--blackColor)
  border 1px solid var(--onBlackColor)
  border-radius 5px
  display flex
  flex-direction column
  justify-content center
  padding 16px
  position fixed
  top 32px
  right 16px
  transform translateX(172px)
  transition transform .5s
  width 120px
  z-index 3

  &--show
    transform translateX(0)

.menu-item
  color var(--onDarkBlueColor)
  font-family var(--fontPrimary)
  margin-bottom 32px
  position relative
  transition color .3s
  width 100%

  a
    border-bottom 2px solid var(--onDarkBlueColor)
    color var(--onDarkBlueColor)
    position absolute
    text-align center
    transition border-bottom .3s
    width 100%

    &:hover
      border-bottom 2px solid var(--onBlackColor)
      color var(--onBlackColor)

</style>