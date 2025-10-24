<template>
  <header-comp/>
  <presentation-comp/>
  <image-separator-comp>
    <img src="/images/waves.svg" alt="Waves Separator">
  </image-separator-comp>
  <projects-comp/>
  <skills-comp/>
  <image-separator-comp>
    <img src="/images/waves_reverse.svg" alt="Waves Separator">
  </image-separator-comp>
  <contact-comp/>
  <portfolio-comp/>
  <image-separator-comp>
    <img src="/images/waves.svg" alt="Waves Separator">
  </image-separator-comp>
  <footer-comp/>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import PresentationComp from './components/PresentationComp.vue'
import SkillsComp from './components/SkillsComp.vue'
import ImageSeparatorComp from './components/ImageSeparatorComp.vue'
import ProjectsComp from './components/ProjectsComp.vue'
import ContactComp from './components/ContactComp.vue'
import PortfolioComp from './components/PortfolioComp.vue'
import FooterComp from './components/FooterComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    PresentationComp,
    SkillsComp,
    ImageSeparatorComp,
    ProjectsComp,
    ContactComp,
    PortfolioComp,
    FooterComp
  }
}
</script>

<style lang="stylus">
.img-wrapper
  height 112px
  width 100%

  img
    height 100%
    width 100%
</style>
