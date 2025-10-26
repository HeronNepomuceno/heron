<template>
  <header class="header">
    <menu-comp/>
    
    <div class="hero-container">
      <div class="content-wrapper">
        <div class="hero-content">
          <div class="text-reveal">
            <span class="greeting">Olá, eu sou</span>
            <h1 class="name">
              <span class="name-part">Heron</span>
              <span class="name-part">Nepomuceno</span>
            </h1>
            <div class="role-wrapper">
              <div class="role-line"></div>
              <h2 class="role">Desenvolvedor Full Stack</h2>
            </div>
          </div>

          <p class="tagline">
            Criando experiências digitais memoráveis com código limpo e design excepcional
          </p>

          <div class="hero-actions">
            <a href="#apresentacao" class="cta-button primary">
              <span>Conheça meu trabalho</span>
              <svg class="arrow-icon" viewBox="0 0 24 24" fill="none">
                <path d="M7 17L17 7M17 7H7M17 7V17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </a>
            <a href="#contato" class="cta-button secondary">
              <span>Vamos conversar</span>
            </a>
          </div>
        </div>

        <div class="hero-visual">
          <div class="visual-container">
            <div class="code-window">
              <div class="window-header">
                <div class="window-dots">
                  <span class="dot red"></span>
                  <span class="dot yellow"></span>
                  <span class="dot green"></span>
                </div>
                <div class="window-title">portfolio.js</div>
              </div>
              <div class="window-content">
                <div class="code-line">
                  <span class="keyword">const </span> 
                  <span class="variable">developer</span> 
                  <span class="operator"> = </span> 
                  <span class="punctuation">{</span>
                </div>
                <div class="code-line indent">
                  <span class="property">name: </span> 
                  <span class="string">'Heron Nepomuceno'</span>
                  <span class="punctuation">,</span>
                </div>
                <div class="code-line indent">
                  <span class="property">role: </span> 
                  <span class="string">'Full Stack Dev'</span>
                  <span class="punctuation">,</span>
                </div>
                <div class="code-line indent">
                  <span class="property">passion: </span> 
                  <span class="string">'Clean Code'</span>
                  <span class="punctuation">,</span>
                </div>
                <div class="code-line indent">
                  <span class="property">skills: </span> 
                  <span class="punctuation">[</span>
                  <span class="string">'Sveltekit'</span>
                  <span class="punctuation">,</span> 
                  <span class="string"> 'Vue'</span>
                  <span class="punctuation">,</span> 
                  <span class="string"> 'React'</span>
                  <span class="punctuation">]</span>
                </div>
                <div class="code-line">
                  <span class="punctuation">}</span>
                  <span class="punctuation">;</span>
                </div>
              </div>
            </div>

            <div class="floating-badge badge-1">
              <svg viewBox="0 0 24 24" fill="none">
                <path d="M9 12L11 14L15 10" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                <circle cx="12" cy="12" r="10" stroke="currentColor" stroke-width="2"/>
              </svg>
              <span>Responsivo</span>
            </div>

            <div class="floating-badge badge-2">
              <svg viewBox="0 0 24 24" fill="none">
                <path d="M13 10V3L4 14H11L11 21L20 10L13 10Z" stroke="currentColor" stroke-width="2"/>
              </svg>
              <span>Performático</span>
            </div>

            <div class="floating-badge badge-3">
              <svg viewBox="0 0 24 24" fill="none">
                <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2"/>
                <path d="M2 17L12 22L22 17M2 12L12 17L22 12" stroke="currentColor" stroke-width="2"/>
              </svg>
              <span>Moderno</span>
            </div>
          </div>
        </div>
      </div>

      <div class="scroll-indicator">
        <div class="mouse">
          <div class="wheel"></div>
        </div>
        <span>Role para explorar</span>
      </div>
    </div>

    <div class="background-effects">
      <div class="gradient-blur blur-1"></div>
      <div class="gradient-blur blur-2"></div>
      <div class="gradient-blur blur-3"></div>
      <div class="grid-pattern"></div>
    </div>
  </header>
</template>

<script>
import MenuComp from './MenuComp.vue'
export default {
  name: 'HeaderComp',
  components: { MenuComp }
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.header
  position relative
  min-height 80vh
  background var(--darkBlueColor)
  overflow hidden
  display flex
  align-items center
  justify-content center

.hero-container
  position relative
  z-index 2
  width 100%
  max-width 1400px
  margin 0 auto
  padding 120px 24px 80px

  @media (min-width: 768px)
    padding 140px 48px 100px

  @media (min-width: 1024px)
    padding 160px 64px 120px

.content-wrapper
  display grid
  grid-template-columns 1fr
  gap 60px
  align-items center

  @media (min-width: 1024px)
    grid-template-columns 1.1fr 0.9fr
    gap 80px

.hero-content
  animation fadeInUp 1s ease-out

.text-reveal
  margin-bottom 32px

.greeting
  display block
  font-family var(--fontSecondary)
  font-size 18px
  color rgba(219, 225, 255, 0.7)
  margin-bottom 16px
  animation slideInLeft 0.8s ease-out

  @media (min-width: 768px)
    font-size 22px

.name
  font-family var(--fontPrimary)
  font-size 48px
  line-height 1.1
  color var(--onDarkBlueColor)
  margin-bottom 20px
  display flex
  flex-direction column

  @media (min-width: 768px)
    font-size 72px

  @media (min-width: 1024px)
    font-size 80px

  .name-part
    display block
    animation slideInLeft 1s ease-out
    
    &:nth-child(1)
      animation-delay 0.2s
      opacity 0
      animation-fill-mode forwards
    
    &:nth-child(2)
      animation-delay 0.4s
      opacity 0
      animation-fill-mode forwards
      background linear-gradient(135deg, var(--onDarkBlueColor), rgba(219, 225, 255, 0.6))
      -webkit-background-clip text
      -webkit-text-fill-color transparent
      background-clip text

.role-wrapper
  display flex
  align-items center
  gap 16px
  animation slideInLeft 1.2s ease-out 0.6s backwards

  .role-line
    width 60px
    height 2px
    background linear-gradient(90deg, rgba(219, 225, 255, 0.8), transparent)

  .role
    font-family var(--fontSecondary)
    font-size 20px
    color rgba(219, 225, 255, 0.9)
    font-weight 500

    @media (min-width: 768px)
      font-size 28px

.tagline
  font-family var(--fontSecondary)
  font-size 16px
  line-height 1.6
  color rgba(219, 225, 255, 0.7)
  margin-bottom 40px
  max-width 500px
  animation fadeInUp 1.4s ease-out 0.8s backwards

  @media (min-width: 768px)
    font-size 18px

.hero-actions
  display flex
  flex-wrap wrap
  gap 16px
  margin-bottom 60px
  animation fadeInUp 1.6s ease-out 1s backwards

.cta-button
  display inline-flex
  align-items center
  gap 10px
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
    background rgba(255, 255, 255, 0.1)
    border-radius 50%
    transform translate(-50%, -50%)
    transition width 0.6s, height 0.6s

  &:hover::before
    width 300px
    height 300px

  .arrow-icon
    width 20px
    height 20px
    transition transform 0.3s ease

  &:hover .arrow-icon
    transform translate(4px, -4px)

.primary
  background linear-gradient(135deg, rgba(219, 225, 255, 0.15), rgba(219, 225, 255, 0.05))
  color var(--onDarkBlueColor)
  border 1px solid rgba(219, 225, 255, 0.3)
  backdrop-filter blur(10px)

  &:hover
    background linear-gradient(135deg, rgba(219, 225, 255, 0.25), rgba(219, 225, 255, 0.15))
    border-color rgba(219, 225, 255, 0.5)
    transform translateY(-2px)

.secondary
  background transparent
  color rgba(219, 225, 255, 0.9)
  border 1px solid rgba(219, 225, 255, 0.3)

  &:hover
    background rgba(219, 225, 255, 0.05)
    border-color rgba(219, 225, 255, 0.5)
    transform translateY(-2px)

.proof-item
  text-align center

  .proof-number
    font-family var(--fontPrimary)
    font-size 32px
    color var(--onDarkBlueColor)
    line-height 1
    margin-bottom 4px

    @media (min-width: 768px)
      font-size 40px

  .proof-label
    font-family var(--fontSecondary)
    font-size 12px
    color rgba(219, 225, 255, 0.6)
    text-transform uppercase
    letter-spacing 1px

.divider
  width 1px
  height 40px
  background linear-gradient(180deg, transparent, rgba(219, 225, 255, 0.3), transparent)

.hero-visual
  animation fadeInRight 1.2s ease-out 0.6s backwards

  @media (max-width: 1023px)
    display flex
    justify-content center

.visual-container
  position relative
  width 100%
  max-width 500px

.code-window
  background rgba(0, 0, 0, 0.4)
  border-radius 12px
  border 1px solid rgba(219, 225, 255, 0.1)
  backdrop-filter blur(10px)
  overflow hidden
  box-shadow 0 20px 60px rgba(0, 0, 0, 0.5)

.window-header
  background rgba(0, 0, 0, 0.3)
  padding 12px 16px
  display flex
  align-items center
  gap 12px
  border-bottom 1px solid rgba(219, 225, 255, 0.1)

.window-dots
  display flex
  gap 6px

  .dot
    width 12px
    height 12px
    border-radius 50%
    
    &.red
      background #ff5f57
    
    &.yellow
      background #ffbd2e
    
    &.green
      background #28ca42

.window-title
  font-family var(--fontSecondary)
  font-size 12px
  color rgba(219, 225, 255, 0.6)

.window-content
  padding 20px
  font-family 'Courier New', monospace
  font-size 14px
  line-height 1.8

  @media (min-width: 768px)
    font-size 16px

.code-line
  animation typingEffect 0.5s ease-out
  
  &.indent
    padding-left 24px

  .keyword
    color #ff79c6
  
  .variable
    color #8be9fd
  
  .operator
    color #ff79c6
  
  .property
    color #50fa7b
  
  .string
    color #f1fa8c
  
  .punctuation
    color #f8f8f2

.floating-badge
  position absolute
  background rgba(219, 225, 255, 0.1)
  backdrop-filter blur(10px)
  border 1px solid rgba(219, 225, 255, 0.2)
  border-radius 100px
  padding 10px 20px
  display flex
  align-items center
  gap 8px
  animation float 3s ease-in-out infinite
  box-shadow 0 10px 30px rgba(0, 0, 0, 0.3)

  svg
    width 20px
    height 20px
    stroke var(--onDarkBlueColor)

  span
    font-family var(--fontSecondary)
    font-size 13px
    font-weight 600
    color var(--onDarkBlueColor)
    white-space nowrap

.badge-1
  top -10px
  right -10px
  animation-delay 0s

.badge-2
  bottom 20%
  left -20px
  animation-delay 1s

  @media (max-width: 1023px)
    left -10px

.badge-3
  bottom -10px
  right 20%
  animation-delay 2s

.scroll-indicator
  position absolute
  bottom 40px
  left 50%
  transform translateX(-50%)
  display flex
  flex-direction column
  align-items center
  gap 12px
  animation fadeIn 2s ease-out 2s backwards

  span
    font-family var(--fontSecondary)
    font-size 12px
    color rgba(219, 225, 255, 0.5)
    text-transform uppercase
    letter-spacing 2px

.mouse
  width 24px
  height 40px
  border 2px solid rgba(219, 225, 255, 0.3)
  border-radius 12px
  position relative

  .wheel
    width 3px
    height 8px
    background rgba(219, 225, 255, 0.5)
    border-radius 2px
    position absolute
    top 8px
    left 50%
    transform translateX(-50%)
    animation scroll 2s ease-in-out infinite

.background-effects
  position absolute
  inset 0
  pointer-events none
  z-index 1

.gradient-blur
  position absolute
  border-radius 50%
  filter blur(100px)
  opacity 0.4

.blur-1
  width 500px
  height 500px
  background linear-gradient(135deg, rgba(40, 65, 144, 0.6), rgba(0, 21, 82, 0.4))
  top -10%
  right -10%
  animation float 8s ease-in-out infinite

.blur-2
  width 400px
  height 400px
  background linear-gradient(135deg, rgba(0, 21, 82, 0.5), rgba(40, 65, 144, 0.3))
  bottom -10%
  left -10%
  animation float 10s ease-in-out infinite
  animation-delay 2s

.blur-3
  width 300px
  height 300px
  background linear-gradient(135deg, rgba(219, 225, 255, 0.1), rgba(40, 65, 144, 0.2))
  top 50%
  left 50%
  transform translate(-50%, -50%)
  animation float 12s ease-in-out infinite
  animation-delay 4s

.grid-pattern
  position absolute
  inset 0
  background linear-gradient(rgba(219, 225, 255, 0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(219, 225, 255, 0.03) 1px, transparent 1px)
  background-size 50px 50px
  opacity 0.5

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

@keyframes fadeIn
  from
    opacity 0
  to
    opacity 1

@keyframes float
  0%, 100%
    transform translateY(0)
  50%
    transform translateY(-15px)

@keyframes scroll
  0%
    opacity 1
    transform translate(-50%, 0)
  100%
    opacity 0
    transform translate(-50%, 20px)

@keyframes typingEffect
  from
    opacity 0
    transform translateX(-10px)
  to
    opacity 1
    transform translateX(0)

// Responsividade adicional para telas pequenas
@media (max-width: 480px)
  .name
    font-size 40px
  
  .role
    font-size 18px
  
  .tagline
    font-size 15px
  
  .cta-button
    width 100%
    justify-content center
  
  .code-window
    font-size 12px
  
  .floating-badge
    padding 8px 16px
    
    span
      font-size 11px
</style>