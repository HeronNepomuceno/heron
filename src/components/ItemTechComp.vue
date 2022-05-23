<template>
  <div class="item-tech">
    <slot></slot>
    <span class="name">{{ tech_name }}</span>
  </div>
</template>

<script>
export default {
  name: "ItemTechComp",
  props: {
    tech_name: String
  }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.item-tech
  align-items center
  display flex
  flex-direction column
  margin-top 32px

.name
  background var(--blackColor)
  border-radius 5px
  font-family var(--fontSecondary)
  font-weight bold
  font-size 18px
  margin-top 16px
  padding 8px 16px

  @media(min-width 600px)
    font-size 22px

  @media(min-width 840px)
    font-size 26px

</style>