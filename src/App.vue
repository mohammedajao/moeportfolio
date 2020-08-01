<template>
  <div id="app">
    <hero id="hero" class="hj-section" />
    <about id="about-me" class="hj-section"/>
    <experience id="experience" class="hj-section"/>
    <projects id="projects" class="hj-section"/>
    <skills />
    <awards id="accolades" class="hj-section"/>
    <contact id="contact" class="hj-section"/>
  </div>
</template>

<script>
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Awards from './components/Accolades.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    Hero,
    About,
    Experience,
    Projects,
    Skills,
    Awards,
    Contact
  }
}
</script>

<style>
body,
html {
	height: 100%;
	width: 100%;
	overflow-x: hidden;
	overflow-y: auto
}

#app {
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-rendering: optimizeLegibility;
	height: 100%
}

.violet {
	color: #8100d8
}

#app .hj_section {
	height: 100vh;
	overflow: hidden;
  margin-bottom: 30px;
}

#app .section-title {
	font-weight: 600;
	color: #696969;
	font-size: 36px;
	display: flex;
	align-items: center
}

#app .section-title,
#app .subtitle {
	font-family: Poppins, sans-serif;
	text-transform: uppercase
}

#app .subtitle {
	font-weight: 800;
	font-size: 60px;
	position: relative;
	color: rgba(0, 0, 0, .7)
}

#app .section-title:before {
	content: attr(sec_num);
	color: rgba(0, 0, 0, .2);
	margin-right: -30px;
	font-size: 72px
}

#app .section-title:after {
	content: " ";
	width: 20%;
	height: 2px;
	margin-left: 10px;
	border: 1px solid #6f6f6f
}

#app .hj-btn {
	text-transform: uppercase;
	border-radius: 5px;
	box-shadow: 0 1px 5px rgba(0, 0, 0, .1);
	text-align: center;
	display: inline-block;
	padding: 10px 20px;
	font-weight: 600;
	border: none;
	margin: 10px 0;
	transition: .5s ease-in-out;
	cursor: pointer;
	text-decoration: none
}

#app .hj-btn.btn-red {
	background-color: #d93333;
	color: #ffec09
}

#app .hj-btn a {
	color: inherit;
	text-decoration: none;
	width: 100%;
	height: 100%
}

#app .hj-btn:hover {
	color: #d93333;
	background-color: #ffec09
}

#app .hj_section>div {
	height: 100%;
	width: 100%;
	margin: 0;
	padding: 0
}

@media (max-width:768px) {
	body #app h3.section-title {
		font-size: 24px
	}
}
</style>
