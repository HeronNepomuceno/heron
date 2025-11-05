<template>
  <section id="contato" class="contact">
    <div class="container">
      <div class="header">
        <h2 class="title">
          Vamos <span class="highlight">Conversar?</span>
        </h2>
        
        <p class="description">
          Estou sempre aberto a novos projetos e oportunidades. Entre em contato e vamos criar algo incrível juntos!
        </p>
      </div>

      <div class="content-wrapper">
        <div class="contact-info">
          <div class="info-card">
            <div class="icon-wrapper">
              <svg viewBox="0 0 24 24" fill="none">
                <path d="M3 8L10.89 13.26C11.2187 13.4793 11.6049 13.5963 12 13.5963C12.3951 13.5963 12.7813 13.4793 13.11 13.26L21 8M5 19H19C19.5304 19 20.0391 18.7893 20.4142 18.4142C20.7893 18.0391 21 17.5304 21 17V7C21 6.46957 20.7893 5.96086 20.4142 5.58579C20.0391 5.21071 19.5304 5 19 5H5C4.46957 5 3.96086 5.21071 3.58579 5.58579C3.21071 5.96086 3 6.46957 3 7V17C3 17.5304 3.21071 18.0391 3.58579 18.4142C3.96086 18.7893 4.46957 19 5 19Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <h3>E-mail</h3>
            <p>heron.developer@gmail.com</p>
          </div>

          <div class="info-card">
            <div class="icon-wrapper">
              <svg viewBox="0 0 24 24" fill="none">
                <path d="M19 4H5C3.89543 4 3 4.89543 3 6V20C3 21.1046 3.89543 22 5 22H19C20.1046 22 21 21.1046 21 20V6C21 4.89543 20.1046 4 19 4Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M8 11H8.01M12 11H12.01M16 11H16.01M8 15H8.01M12 15H12.01M16 15H16.01M8 19H8.01M12 19H12.01M16 19H16.01M8 7H16" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <h3>WhatsApp</h3>
            <p>(86) 99594-1993</p>
          </div>

          <a href="https://www.linkedin.com/in/heron-nepomuceno-b3125b1b6" target="_blank" class="social-link">
            <svg class="social-icon" viewBox="0 0 24 24">
              <use xlink:href="/images/icons/sprite.svg#linkedin"></use>
            </svg>
            <span>Conecte-se no LinkedIn</span>
            <svg class="arrow-icon" viewBox="0 0 24 24" fill="none">
              <path d="M7 17L17 7M17 7H7M17 7V17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </a>
        </div>

        <form class="contact-form" action="https://formsubmit.co/heron.developer@gmail.com" method="POST">
          <div class="form-group">
            <label for="nome">Nome</label>
            <input 
              id="nome"
              type="text" 
              name="nome" 
              placeholder="Seu nome completo" 
              required
            >
          </div>

          <div class="form-group">
            <label for="email">E-mail</label>
            <input 
              id="email"
              type="email" 
              name="email" 
              placeholder="seu@email.com" 
              required
            >
          </div>

          <div class="form-group">
            <label for="assunto">Assunto</label>
            <input 
              id="assunto"
              type="text" 
              name="assunto" 
              placeholder="Sobre o que deseja falar?" 
              required
            >
          </div>

          <div class="form-group">
            <label for="mensagem">Mensagem</label>
            <textarea 
              id="mensagem"
              name="mensagem" 
              placeholder="Conte-me mais sobre seu projeto ou ideia..."
              rows="5"
              required
            ></textarea>
          </div>

          <input 
            type="hidden" 
            name="_autoresponse" 
            value="Olá! Recebi sua mensagem e responderei o mais breve possível. Obrigado pelo contato!"
          >

          <button type="submit" class="submit-button">
            <span>Enviar Mensagem</span>
            <svg viewBox="0 0 24 24" fill="none">
              <path d="M22 2L11 13M22 2L15 22L11 13M22 2L2 9L11 13" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </button>
        </form>
      </div>
    </div>

    <div class="background-effects">
      <div class="gradient-blur blur-1"></div>
      <div class="gradient-blur blur-2"></div>
      <div class="grid-pattern"></div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactComp"
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.contact
  position relative
  min-height 90vh
  background var(--onDarkBlueColor)
  padding 80px 24px
  overflow hidden

  @media (min-width: 768px)
    padding 100px 48px

  @media (min-width: 1024px)
    padding 120px 64px

.container
  max-width 1400px
  margin 0 auto
  position relative
  z-index 2

.header
  text-align center
  margin-bottom 64px
  animation fadeInUp 0.8s ease-out

  @media (min-width: 768px)
    margin-bottom 80px

.title
  font-family var(--fontPrimary)
  font-size 36px
  line-height 1.2
  color var(--darkBlueColor)
  margin-bottom 24px

  @media (min-width: 768px)
    font-size 48px

  @media (min-width: 1024px)
    font-size 56px

  .highlight
    background linear-gradient(135deg, var(--darkBlueColor), #284190)
    -webkit-background-clip text
    -webkit-text-fill-color transparent
    background-clip text

.description
  font-family var(--fontSecondary)
  font-size 16px
  line-height 1.6
  color rgba(0, 21, 82, 0.7)
  max-width 600px
  margin 0 auto

  @media (min-width: 768px)
    font-size 18px

.content-wrapper
  display grid
  grid-template-columns 1fr
  gap 48px
  align-items start

  @media (min-width: 1024px)
    grid-template-columns 400px 1fr
    gap 64px

.contact-info
  display flex
  flex-direction column
  gap 20px
  animation fadeInLeft 1s ease-out 0.4s backwards

.info-card
  background linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.6))
  border 1px solid rgba(0, 21, 82, 0.1)
  border-radius 20px
  padding 24px
  backdrop-filter blur(10px)
  transition transform 0.3s ease, box-shadow 0.3s ease

  &:hover
    transform translateY(-5px)
    box-shadow 0 10px 30px rgba(0, 21, 82, 0.15)

  .icon-wrapper
    width 48px
    height 48px
    background linear-gradient(135deg, var(--darkBlueColor), #284190)
    border-radius 12px
    display flex
    align-items center
    justify-content center
    margin-bottom 16px

    svg
      width 24px
      height 24px
      stroke var(--onDarkBlueColor)

  h3
    font-family var(--fontPrimary)
    font-size 18px
    color var(--darkBlueColor)
    margin-bottom 8px

  p
    font-family var(--fontSecondary)
    font-size 15px
    color rgba(0, 21, 82, 0.7)
    word-break break-word

.social-link
  display flex
  align-items center
  gap 12px
  padding 20px 24px
  background linear-gradient(135deg, var(--darkBlueColor), #284190)
  border-radius 20px
  color var(--onDarkBlueColor)
  text-decoration none
  transition all 0.3s ease
  position relative
  overflow hidden

  &::before
    content ''
    position absolute
    top 50%
    left 50%
    width 0
    height 0
    background rgba(255, 255, 255, 0.1)
    border-radius 50%
    transform translate(-50%, -50%)
    transition width 0.6s, height 0.6s

  &:hover::before
    width 300px
    height 300px

  &:hover
    transform translateY(-2px)
    box-shadow 0 10px 30px rgba(0, 21, 82, 0.3)

  .social-icon
    width 24px
    height 24px
    fill currentColor
    flex-shrink 0

  span
    font-family var(--fontSecondary)
    font-size 16px
    font-weight 600
    flex 1

  .arrow-icon
    width 20px
    height 20px
    stroke currentColor
    transition transform 0.3s ease

  &:hover .arrow-icon
    transform translate(4px, -4px)

.contact-form
  background rgba(255, 255, 255, 0.8)
  backdrop-filter blur(10px)
  border 1px solid rgba(0, 21, 82, 0.1)
  border-radius 24px
  padding 32px
  animation fadeInRight 1s ease-out 0.6s backwards

  @media (min-width: 768px)
    padding 40px

.form-group
  margin-bottom 24px

  label
    display block
    font-family var(--fontSecondary)
    font-size 14px
    font-weight 600
    color var(--darkBlueColor)
    margin-bottom 8px

    @media (min-width: 768px)
      font-size 15px

  input, textarea
    width 100%
    padding 14px 16px
    background rgba(255, 255, 255, 0.9)
    border 2px solid rgba(0, 21, 82, 0.1)
    border-radius 12px
    font-family var(--fontSecondary)
    font-size 15px
    color var(--darkBlueColor)
    transition all 0.3s ease
    box-sizing border-box

    &::placeholder
      color rgba(0, 21, 82, 0.4)

    &:focus
      outline none
      border-color var(--darkBlueColor)
      box-shadow 0 0 0 4px rgba(0, 21, 82, 0.1)

  textarea
    resize vertical
    min-height 120px

.submit-button
  width 100%
  display flex
  align-items center
  justify-content center
  gap 12px
  padding 16px 32px
  background linear-gradient(135deg, var(--darkBlueColor), #284190)
  border none
  border-radius 100px
  color var(--onDarkBlueColor)
  font-family var(--fontSecondary)
  font-size 16px
  font-weight 600
  cursor pointer
  transition all 0.3s ease
  position relative
  overflow hidden

  &::before
    content ''
    position absolute
    top 50%
    left 50%
    width 0
    height 0
    background rgba(255, 255, 255, 0.2)
    border-radius 50%
    transform translate(-50%, -50%)
    transition width 0.6s, height 0.6s

  &:hover::before
    width 400px
    height 400px

  &:hover
    transform translateY(-2px)
    box-shadow 0 10px 30px rgba(0, 21, 82, 0.3)

  svg
    width 20px
    height 20px
    stroke currentColor
    transition transform 0.3s ease

  &:hover svg
    transform translateX(4px)

.background-effects
  position absolute
  inset 0
  pointer-events none
  z-index 1

.gradient-blur
  position absolute
  border-radius 50%
  filter blur(100px)
  opacity 0.3

.blur-1
  width 500px
  height 500px
  background linear-gradient(135deg, rgba(0, 21, 82, 0.3), rgba(40, 65, 144, 0.2))
  top -10%
  left -10%
  animation float 8s ease-in-out infinite

.blur-2
  width 400px
  height 400px
  background linear-gradient(135deg, rgba(40, 65, 144, 0.2), rgba(219, 225, 255, 0.3))
  bottom -10%
  right -10%
  animation float 10s ease-in-out infinite
  animation-delay 2s

.grid-pattern
  position absolute
  inset 0
  background linear-gradient(rgba(0, 21, 82, 0.02) 1px, transparent 1px), linear-gradient(90deg, rgba(0, 21, 82, 0.02) 1px, transparent 1px)
  background-size 50px 50px
  opacity 0.5

@keyframes fadeInUp
  from
    opacity 0
    transform translateY(30px)
  to
    opacity 1
    transform translateY(0)

@keyframes fadeInLeft
  from
    opacity 0
    transform translateX(-30px)
  to
    opacity 1
    transform translateX(0)

@keyframes fadeInRight
  from
    opacity 0
    transform translateX(30px)
  to
    opacity 1
    transform translateX(0)

@keyframes float
  0%, 100%
    transform translateY(0)
  50%
    transform translateY(-20px)
</style>