<template>
	<section id="projetos" class="projects">
		<div class="container">
			<div class="header">
				<div class="badge">
					<svg class="badge-icon" viewBox="0 0 24 24" fill="none">
						<path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					<span>Portfólio</span>
				</div>
				
				<h2 class="title">
					<span class="highlight">Projetos</span> em Destaque
				</h2>
				
				<p class="description">
					Uma seleção dos meus trabalhos mais recentes, onde transformei ideias em soluções digitais funcionais e elegantes.
				</p>
			</div>

		<div class="projects-grid">
			<item-project-comp 
				project_name="Estética Unitá" 
				project_image="project_unita.svg"
				project_info="Website desenvolvido para uma clínica de estética, com foco em apresentar os serviços, a equipe e o espaço de atendimento. O projeto priorizou a experiência do usuário, responsividade e a identidade visual da clínica, garantindo uma presença online elegante e acessível."
				:project_link="project_link_unita"
				:project_github="project_github_unita"/>

			<item-project-comp 
				project_name="Hoteleiro" 
				project_image="project_hoteleiro.svg"
				project_info="Website desenvolvido para minha startup Hoteleiro, vencedora do programa Startup Nordeste 2025. O projeto tem como objetivo apresentar nossa solução de gestão hoteleira de forma intuitiva, destacando a proposta da empresa e a experiência do usuário."
				:project_link="project_link_hoteleiro"
				:project_github="project_github_hoteleiro"/>

				<item-project-comp 
				project_name="Pricecryp" 
				project_image="project_pricecryp.svg"
				project_info="Projeto desenvolvido para mostrar, em tempo real, os preços das criptomoedas, através do consumo da API da CoinGecko."
				:project_link="project_link_pricecryp"
				:project_github="project_github_pricecryp"/>

				<item-project-comp 
				project_name="Website Maejr" 
				project_image="project_maejr.svg"
				project_info="Projeto desenvolvido para um cliente que solicitou a produção de um website para sua empresa. O site foi feito nos moldes da identidade visual da empresa, utilizando de suas cores, fontes e logos da melhor forma possível."
				:project_link="project_link_maejr"
				:project_github="project_github_maejr"/>

				<item-project-comp 
				project_name="Jogo de Bebidas" 
				project_image="project_atecair.svg"
				project_info="Projeto desenvolvido fruto de uma conversa entre amigos que buscavam ideias para se divertir em eventos sociais."
				:project_link="project_link_atecair"
				:project_github="project_github_atecair"/>
			</div>

		</div>
	</section>
</template>

<script>
import TitleComp from './TitleComp.vue'
import ItemProjectComp from './ItemProjectComp.vue'
export default {
	name: 'ProjectsComp',
	components: {
		TitleComp,
		ItemProjectComp
	},
	data: function () {
    return {
      project_link_unita: "https://unita-estetica.netlify.app/",
      project_github_unita: "https://github.com/HeronNepomuceno/unita-site",

      project_link_hoteleiro: "https://hoteleiro.app/",
      project_github_hoteleiro: "http://www.pi.gov.br/startup-hoteleiro-estudantes-da-uespi-transformam-ideia-em-negocio-inovador/",

      project_link_pricecryp: "https://heronnepomuceno.github.io/pricecryp/",
      project_github_pricecryp: "https://github.com/HeronNepomuceno/pricecryp",

      project_link_maejr: "https://maejr.netlify.app/",
      project_github_maejr: "https://github.com/catiuespi/maejr",

      project_link_atecair: "https://atecair.netlify.app/",
      project_github_atecair: "https://github.com/HeronNepomuceno/ate-cair",

      project_link_webgame: "https://www.linkedin.com/feed/update/urn:li:activity:6902715882272108545/",
      project_github_webgame: "https://github.com/HeronNepomuceno/paladino-vs-dragao",

      project_link_cssorder: "https://css-order-caker.netlify.app/",
      project_github_cssorder: "https://github.com/HeronNepomuceno/css-order-caker"
    }
  },
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.projects
	position relative
	min-height 80vh
	background var(--darkBlueColor)
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

.badge
	display inline-flex
	align-items center
	gap 8px
	background linear-gradient(135deg, rgba(219, 225, 255, 0.1), rgba(219, 225, 255, 0.05))
	border 1px solid rgba(219, 225, 255, 0.2)
	border-radius 100px
	padding 8px 20px
	margin-bottom 24px
	backdrop-filter blur(10px)

	.badge-icon
		width 20px
		height 20px
		stroke var(--onDarkBlueColor)

	span
		font-family var(--fontSecondary)
		font-size 14px
		font-weight 600
		color var(--onDarkBlueColor)

		@media (min-width: 768px)
			font-size 16px

.title
	font-family var(--fontPrimary)
	font-size 36px
	line-height 1.2
	color var(--onDarkBlueColor)
	margin-bottom 24px

	@media (min-width: 768px)
		font-size 48px

	@media (min-width: 1024px)
		font-size 56px

	.highlight
		background linear-gradient(135deg, var(--onDarkBlueColor), rgba(219, 225, 255, 0.7))
		-webkit-background-clip text
		-webkit-text-fill-color transparent
		background-clip text

.description
	font-family var(--fontSecondary)
	font-size 16px
	line-height 1.6
	color rgba(219, 225, 255, 0.7)
	max-width 600px
	margin 0 auto

	@media (min-width: 768px)
		font-size 18px

.projects-grid
	display grid
	grid-template-columns 1fr
	gap 32px
	justify-items center
	
	@media (min-width: 768px)
		grid-template-columns repeat(2, 1fr)
		gap 40px

	@media (min-width: 1200px)
		grid-template-columns repeat(3, 1fr)
		gap 48px

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
	background linear-gradient(135deg, rgba(40, 65, 144, 0.4), rgba(0, 21, 82, 0.3))
	top -10%
	left -10%
	animation float 8s ease-in-out infinite

.blur-2
	width 400px
	height 400px
	background linear-gradient(135deg, rgba(219, 225, 255, 0.2), rgba(40, 65, 144, 0.2))
	bottom -10%
	right -10%
	animation float 10s ease-in-out infinite
	animation-delay 2s

.grid-pattern
	position absolute
	inset 0
	background linear-gradient(rgba(219, 225, 255, 0.02) 1px, transparent 1px), linear-gradient(90deg, rgba(219, 225, 255, 0.02) 1px, transparent 1px)
	background-size 50px 50px
	opacity 0.5

@keyframes fadeInUp
	from
		opacity 0
		transform translateY(30px)
	to
		opacity 1
		transform translateY(0)

@keyframes float
	0%, 100%
		transform translateY(0)
	50%
		transform translateY(-20px)
</style>