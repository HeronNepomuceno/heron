<template>
  <section id="apresentacao" class="presentation">
    <div class="container">
      <div class="content-wrapper">
        <div class="text-content">
          <div class="badge">
            <svg class="badge-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <span>Desenvolvedor Full Stack</span>
          </div>
          
          <h2 class="main-title ">
            <span class="highlight">Sobre min</span>
          </h2>
          
          <p class="description">
            Sou <strong>Heron Nepomuceno</strong>, desenvolvedor com mais de 4 anos de experiência na criação de sites, sistemas e aplicações web. Bacharel em Ciência da Computação pela Universidade Estadual do Piauí, tenho paixão por transformar ideias em soluções digitais que unem design intuitivo, desempenho e propósito.
          </p>

          <div class="stats-grid">
            <div class="stat-item">
              <div class="stat-number">4+</div>
              <div class="stat-label">Anos de experiência</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">50+</div>
              <div class="stat-label">Projetos concluídos</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">100%</div>
              <div class="stat-label">Dedicação</div>
            </div>
          </div>

          <div class="cta-buttons">
            <a href="#projetos" class="btn btn-primary">
              Ver Projetos
              <svg class="btn-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M5 12H19M19 12L12 5M19 12L12 19" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </a>
            <a href="#contato" class="btn btn-secondary">
              Entre em Contato
            </a>
          </div>
        </div>

        <div class="image-content">
          <div class="image-container">
            <div class="image-background"></div>
            <img class="profile-image" src="/images/presentation.jpg" alt="Heron Nepomuceno - Desenvolvedor Full Stack">
            <div class="floating-card card-1">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M9 12L11 14L15 10M21 12C21 16.9706 16.9706 21 12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3C16.9706 3 21 7.02944 21 12Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span>Clean Code</span>
            </div>
            <div class="floating-card card-2">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M13 10V3L4 14H11L11 21L20 10L13 10Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span>Fast Performance</span>
            </div>
            <div class="floating-card card-3">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span>Modern Stack</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="decorative-elements">
      <div class="dot-grid"></div>
      <div class="gradient-orb orb-1"></div>
      <div class="gradient-orb orb-2"></div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PresentationComp'
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.presentation
  position relative
  background var(--onDarkBlueColor)
  min-height 60vh
  display flex
  align-items center
  padding 80px 24px
  overflow hidden

  @media (min-width: 768px)
    padding 100px 48px

  @media (min-width: 1024px)
    padding 120px 64px

.container
  max-width 1400px
  margin 0 auto
  width 100%
  position relative
  z-index 2

.content-wrapper
  display grid
  grid-template-columns 1fr
  gap 48px
  align-items center

  @media (min-width: 1024px)
    grid-template-columns 1.2fr 1fr
    gap 80px

.text-content
  animation fadeInUp 0.8s ease-out

.badge
  display inline-flex
  align-items center
  gap 8px
  background linear-gradient(135deg, rgba(0, 21, 82, 0.1), rgba(0, 21, 82, 0.05))
  border 1px solid rgba(0, 21, 82, 0.2)
  border-radius 100px
  padding 8px 20px
  margin-bottom 24px
  backdrop-filter blur(10px)
  animation slideInLeft 0.6s ease-out

  .badge-icon
    width 20px
    height 20px
    stroke var(--darkBlueColor)

  span
    font-family var(--fontSecondary)
    font-size 14px
    font-weight 600
    color var(--darkBlueColor)

    @media (min-width: 768px)
      font-size 16px

.main-title
  font-family var(--fontPrimary)
  font-size 36px
  line-height 1.2
  color var(--darkBlueColor)
  margin-bottom 32px
  animation slideInLeft 0.8s ease-out 0.2s backwards

  @media (min-width: 768px)
    font-size 48px

  @media (min-width: 1024px)
    font-size 52px

  .highlight
    background linear-gradient(135deg, var(--darkBlueColor), #284190)
    -webkit-background-clip text
    -webkit-text-fill-color transparent
    background-clip text
    position relative
    display inline-block

    &::after
      content ''
      position absolute
      left 0
      bottom -4px
      width 100%
      height 3px
      background linear-gradient(90deg, var(--darkBlueColor), transparent)
      border-radius 2px

.description
  font-family var(--fontSecondary)
  font-size 16px
  line-height 1.8
  color rgba(0, 21, 82, 0.8)
  margin-bottom 40px
  animation slideInLeft 1s ease-out 0.4s backwards

  @media (min-width: 768px)
    font-size 18px

  strong
    color var(--darkBlueColor)
    font-weight 700

.stats-grid
  display grid
  grid-template-columns repeat(3, 1fr)
  gap 24px
  margin-bottom 40px
  animation slideInLeft 1.2s ease-out 0.6s backwards

  @media (min-width: 768px)
    gap 32px

.stat-item
  text-align center
  padding 20px
  background linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.6))
  border-radius 16px
  border 1px solid rgba(0, 21, 82, 0.1)
  backdrop-filter blur(10px)
  transition transform 0.3s ease, box-shadow 0.3s ease

  &:hover
    transform translateY(-5px)
    box-shadow 0 10px 30px rgba(0, 21, 82, 0.15)

  .stat-number
    font-family var(--fontPrimary)
    font-size 32px
    color var(--darkBlueColor)
    margin-bottom 8px

    @media (min-width: 768px)
      font-size 40px

  .stat-label
    font-family var(--fontSecondary)
    font-size 12px
    color rgba(0, 21, 82, 0.7)
    font-weight 500

    @media (min-width: 768px)
      font-size 14px

.cta-buttons
  display flex
  flex-wrap wrap
  gap 16px
  animation slideInLeft 1.4s ease-out 0.8s backwards

.btn
  display inline-flex
  align-items center
  gap 8px
  padding 16px 32px
  border-radius 100px
  font-family var(--fontSecondary)
  font-size 16px
  font-weight 600
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
    border-radius 50%
    background rgba(255, 255, 255, 0.2)
    transform translate(-50%, -50%)
    transition width 0.6s, height 0.6s

  &:hover::before
    width 300px
    height 300px

  .btn-icon
    width 20px
    height 20px
    transition transform 0.3s ease

  &:hover .btn-icon
    transform translateX(4px)

.btn-primary
  background linear-gradient(135deg, var(--darkBlueColor), #284190)
  color var(--onDarkBlueColor)
  box-shadow 0 10px 30px rgba(0, 21, 82, 0.3)

  &:hover
    transform translateY(-2px)
    box-shadow 0 15px 40px rgba(0, 21, 82, 0.4)

.btn-secondary
  background transparent
  color var(--darkBlueColor)
  border 2px solid var(--darkBlueColor)

  &:hover
    background var(--darkBlueColor)
    color var(--onDarkBlueColor)
    transform translateY(-2px)

.image-content
  animation fadeInRight 1s ease-out 0.4s backwards

  @media (max-width: 1023px)
    display flex
    justify-content center

.image-container
  position relative
  width 100%
  max-width 500px
  aspect-ratio 1
  margin 0 auto

.image-background
  position absolute
  inset -20px
  background linear-gradient(135deg, rgba(0, 21, 82, 0.1), rgba(40, 65, 144, 0.1))
  border-radius 30% 70% 70% 30% / 30% 30% 70% 70%
  animation morph 8s ease-in-out infinite
  z-index 0

.profile-image
  position relative
  width 100%
  height 100%
  object-fit cover
  border-radius 30px
  border 4px solid rgba(255, 255, 255, 0.8)
  box-shadow 0 20px 60px rgba(0, 21, 82, 0.2)
  z-index 1

.floating-card
  position absolute
  background rgba(255, 255, 255, 0.95)
  backdrop-filter blur(10px)
  border 1px solid rgba(0, 21, 82, 0.1)
  border-radius 16px
  padding 12px 20px
  display flex
  align-items center
  gap 10px
  box-shadow 0 10px 30px rgba(0, 21, 82, 0.15)
  z-index 2
  animation float 3s ease-in-out infinite

  svg
    width 24px
    height 24px
    stroke var(--darkBlueColor)

  span
    font-family var(--fontSecondary)
    font-size 14px
    font-weight 600
    color var(--darkBlueColor)
    white-space nowrap

.card-1
  top 10%
  right -10%
  animation-delay 0s

  @media (max-width: 1023px)
    top 5%
    right -5%

.card-2
  bottom 25%
  left -15%
  animation-delay 1s

  @media (max-width: 1023px)
    bottom 20%
    left -10%

.card-3
  bottom 5%
  right -5%
  animation-delay 2s

  @media (max-width: 1023px)
    bottom 0%
    right 0%

.decorative-elements
  position absolute
  inset 0
  pointer-events none
  z-index 1

.dot-grid
  position absolute
  top 10%
  right 10%
  width 200px
  height 200px
  background-image radial-gradient(circle, rgba(0, 21, 82, 0.15) 1px, transparent 1px)
  background-size 20px 20px
  opacity 0.5
  animation float 4s ease-in-out infinite

.gradient-orb
  position absolute
  border-radius 50%
  filter blur(80px)
  opacity 0.3
  animation float 6s ease-in-out infinite

.orb-1
  width 400px
  height 400px
  background linear-gradient(135deg, rgba(0, 21, 82, 0.3), rgba(40, 65, 144, 0.2))
  top -10%
  left -10%
  animation-delay 0s

.orb-2
  width 300px
  height 300px
  background linear-gradient(135deg, rgba(40, 65, 144, 0.2), rgba(219, 225, 255, 0.3))
  bottom -5%
  right -5%
  animation-delay 3s

@keyframes fadeInUp
  from
    opacity 0
    transform translateY(30px)
  to
    opacity 1
    transform translateY(0)

@keyframes fadeInRight
  from
    opacity 0
    transform translateX(-30px)
  to
    opacity 1
    transform translateX(0)

@keyframes slideInLeft
  from
    opacity 0
    transform translateX(-30px)
  to
    opacity 1
    transform translateX(0)

@keyframes float
  0%, 100%
    transform translateY(0)
  50%
    transform translateY(-20px)

@keyframes morph
  0%, 100%
    border-radius 30% 70% 70% 30% / 30% 30% 70% 70%
  25%
    border-radius 58% 42% 75% 25% / 76% 46% 54% 24%
  50%
    border-radius 50% 50% 33% 67% / 55% 27% 73% 45%
  75%
    border-radius 33% 67% 58% 42% / 63% 68% 32% 37%
</style>