<template>
  <section id="apresentacao" class="presentation">
    <title-comp title="Sobre mim" :color_blue_status="true"/>
    <div class="group-section">
      <span class="info">
        Sou Heron Nepomuceno, desenvolvedor com mais de 4 anos de experiência na criação de sites, sistemas e aplicações web.
        Bacharel em Ciência da Computação pela Universidade Estadual do Piauí, tenho paixão por transformar ideias em soluções digitais que unem design intuitivo, desempenho e propósito.
      </span>
      <div class="image-wrapper">
        <img class="image" src="/images/presentation.jpg" alt="Presentation Hello">
      </div>
    </div>
  </section>
</template>

<script>
import TitleComp from './TitleComp.vue'
export default {
  name: 'PresentationComp',
  components: {
    TitleComp
  }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.background
  background #000

.presentation
  align-items center
  background var(--onDarkBlueColor)
  color var(--darkBlueColor)
  display flex
  flex-direction column
  padding 48px 16px
  width calc(100% - 32px)

  @media (min-width: 840px)
    padding 48px 64px
    width calc(100% - 128px)

.group-section
  align-items center
  display flex
  flex-direction column
  justify-content center
  width 100%

  @media (min-width: 840px)
    flex-direction row

.info
  font-size 16px
  font-weight 400
  text-align center
  width 100%

  @media (min-width: 600px)
    font-size 18px
    margin-right 16px

  @media (min-width: 840px)
    font-size 26px

  &::first-letter
    font-size 48px

    @media (min-width: 840px)
      font-size 68px

.image-wrapper
  align-items center
  display flex
  height 100%
  justify-content center
  margin-top 32px
  width 100%

.image
  background rgba(0, 0, 0, 0.5)
  border-radius 16px
  height 300px
  padding 0 16px
  width 300px

  @media (min-width: 840px)
    height 400px
    width 400px
</style>