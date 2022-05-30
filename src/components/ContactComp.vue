<template>
  <section id="contato" class="contact">
    <title-comp title="Contato" :color_blue_status="true"/>
    <span class="contact__info">
      Entre em contato comigo através do meu linkedin ou e-mail preenchendo o formulário abaixo:
    </span>
    <div class="contact__itens">
      <form class="contact__form" action="https://formsubmit.co/heronnepo1@gmail.com" method="POST">
        <label class="label-wrapper">
          <span class="label">Nome:</span>
          <input class="input" type="text" name="nome" placeholder="Nome pessoal ou institucional" required>
        </label>
        <label class="label-wrapper">
          <span class="label">E-mail:</span>
          <input class="input" type="email" name="email" placeholder="Exemplo@gmail.com" required>
        </label>
        <label class="label-wrapper">
          <span class="label">Assunto:</span>
          <input class="input" type="text" name="assunto" placeholder="Tema da mensagem" required>
        </label>
        <label class="label-wrapper">
          <span class="label">Mensagem:</span>
          <textarea class="textarea" name="mensagem" placeholder="" required></textarea>
        </label>
        <input type="hidden" name="_autoresponse" value="Olá, passando aqui para confirmar o envio do seu e-mail, e responderei o mais rápido possível!">
        <div class="footer">
          <a class="link" href="https://www.linkedin.com/in/heron-nepomuceno-b3125b1b6">
          	<svg class="icon">
						  <use xlink:href="/images/icons/sprite.svg#linkedin"></use>
					  </svg>
            <span>Acessar Linkedin</span>
          </a>
          <button class="button" type="submit">Enviar</button>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
import TitleComp from './TitleComp.vue'
export default {
	name: "ContactComp",
	components: { TitleComp }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.contact
  align-items center
  background var(--onDarkBlueColor)
  color var(--onDarkBlueColor)
  display flex
  flex-direction column
  font-family var(--fontSecondary)
  padding 48px 32px 64px 32px
  width calc(100% - 64px)

  &__itens
    align-items center
    display flex
    flex-direction column
    justify-content space-evenly
    width 100%

    @media (min-width: 1080px)
      align-items stretch
      flex-direction row-reverse

  &__info
    color var(--darkBlueColor)
    font-size 18px
    text-align center
    width 100%

    @media (min-width: 600px)
      font-size 22px
      max-width 1000px

    &::first-letter
      font-size 36px

  &__form
    align-items center
    background var(--darkBlueColor)
    border solid 2px var(--blackColor)
    border-radius 6px
    display flex
    flex-direction column
    height 100%
    justify-content center
    margin-top 32px
    padding 32px 16px
    width 100%

    @media (min-width: 600px)
      max-width 480px

    @media (min-width: 840px)
      max-width 640px

    @media (min-width: 1080px)
      margin-left 48px

    .label-wrapper
      align-items flex-start
      display flex
      flex-direction column
      justify-content center
      margin-bottom 16px
      width 100%

      .label
        font-size 14px
        margin-bottom 8px
        margin-left 4px

        @media (min-width: 600px)
          font-size 16px

        @media (min-width: 840px)
          font-size 18px

    .input, .textarea
      background var(--darkBlueColor)
      border 1.6px solid var(--onDarkBlueColor)
      border-radius 6px
      color var(--onDarkBlueColor)
      font-size 14px
      height 32px
      margin-bottom 8px
      padding-left 4px
      transition background .3s
      width 100%

      @media (min-width: 600px)
        font-size 16px

      @media (min-width: 840px)
        font-size 18px

    .textarea
      height 100px
      font-family var(--fontSecondary)

    .footer
      align-items center
      display flex
      justify-content space-between
      margin-top 16px
      width 100%

    .button
      background var(--onDarkBlueColor)
      border-radius 16px
      color var(--darkBlueColor)
      font-family var(--fontSecondary)
      font-size 14px
      height 32px
      padding 0 32px

      @media (min-width: 600px)
        font-size 16px

      @media (min-width: 840px)
        font-size 18px

      &:hover
        opacity .8

    .link
      align-items center
      border 1px solid var(--onDarkBlueColor)
      border-radius 16px
      color var(--onDarkBlueColor)
      display flex
      font-family var(--fontSecondary)
      font-size 14px
      height 32px
      margin-right 16px
      padding 0 24px

      @media (min-width: 600px)
        font-size 16px

      @media (min-width: 840px)
        font-size 18px

      &:hover
        opacity .8

    .icon
      fill currentcolor
      height 24px
      margin-right 16px
      width 24px

      @media (min-width: 600px)
        height 28px
        width 28px

      @media (min-width: 840px)
        height 32px
        width 32px

.image-wrapper
  align-items center
  display none
  height 100%
  justify-content center
  margin-left 32px
  margin-top 32px
  width 400px

  @media (min-width: 1080px)
    display flex

.image
  border-radius 16px
  height 360px
  padding 0 16px
  width 360px

</style>