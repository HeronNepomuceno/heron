<template>
	<section id="projetos" class="projects">
		<title-comp title="Projetos" :color_white_status="true"/>
		<div class="item-project-wrapper">

			<item-project-comp 
			project_name="Pricecryp" 
			project_image="project_pricecryp.svg"
			project_info="Projeto desenvolvido para mostrar, em tempo real, os preços das criptomoedas, através do consumo da API da CoinGecko."
			:project_link="project_link_pricecryp"
			:project_github="project_github_pricecryp"/>

			<item-project-comp 
			project_name="Portfólio 1.0" 
			project_image="project_portfoliov1.svg"
			project_info="Projeto desenvolvido nos padrões pessoais de design e funcionalidade, considerando sempre a responsividade e a melhor experiência do usuário independente do dispositivo que o mesmo esteja usando"
			:project_link="project_link_portfoliov1"
			:project_github="project_github_portfoliov1"/>

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

			<item-project-comp 
			project_name="Website FUAPI" 
			project_image="project_fuapi.svg"
			project_info="O projeto trata-se de um website informativo sobre a Fundação de Apoio ao Desenvolvimento Educacional, Governança e Meio Ambiente da UESPI."
			:project_link="project_link_fuapi"
			:project_github="project_github_fuapi"/>

			<item-project-comp 
			project_name="CSS Order Caker" 
			project_image="project_cssorder.svg"
			project_info="O projeto consiste em criar uma ferramenta capaz de organizar o CSS do programador em ordem alfabética, para que o código fique mais legível e intuitivo."
			:project_link="project_link_cssorder"
			:project_github="project_github_cssorder"/>

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
      project_link_pricecryp: "https://heronnepomuceno.github.io/pricecryp/",
      project_github_pricecryp: "https://github.com/HeronNepomuceno/pricecryp",

      project_link_portfoliov1: "https://herondev.netlify.app/",
      project_github_portfoliov1: "https://github.com/HeronNepomuceno/portfolio",

      project_link_maejr: "https://maejr.netlify.app/",
      project_github_maejr: "https://github.com/catiuespi/maejr",

      project_link_atecair: "https://atecair.netlify.app/",
      project_github_atecair: "https://github.com/HeronNepomuceno/ate-cair",

      project_link_webgame: "https://www.linkedin.com/feed/update/urn:li:activity:6902715882272108545/",
      project_github_webgame: "https://github.com/HeronNepomuceno/paladino-vs-dragao",

      project_link_fuapi: "https://fuapi.netlify.app/",
      project_github_fuapi: "https://github.com/HeronNepomuceno/FUAPI",

      project_link_cssorder: "https://css-order-caker.netlify.app/",
      project_github_cssorder: "https://github.com/HeronNepomuceno/css-order-caker"
    }
  },
}
</script>

<style lang="stylus" scoped>
@import '../assets/style/global.styl'

.projects
	align-items center
	display flex
	flex-direction column
	height 100%
	padding 48px 32px
	width calc(100% - 64px)

.item-project-wrapper
	align-items center
	display flex
	flex-direction column
	justify-content center
	margin-top 16px
	width 100%

	@media(min-width 840px)
		display inline-grid
		grid-template-columns 1fr 1fr
		grid-gap 16px
		justify-items center
		align-items center

	@media(min-width 1080px)
		grid-template-columns 1fr 1fr 1fr

</style>