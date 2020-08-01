<template lang="html">
  <div class="d-flex">
     <div class="main_nav d-none d-md-inline-block">
       <a v-for="(image, link) in this.nav" :key="link" :href="link"><i :class="image"></i></a>
     </div>
     <div class="hero d-inline-block">
        <span>
           <div class="d-inline-block h-rule"></div>
           <p class="d-inline-block">Mohammed Ajao | Software Engineer</p>
        </span>
        <h1>Elegance is simplicity but refined and understood.</h1>
        <p>I'm a software engineer based in New York City. I build and design full-stack applications and games. My products are created by looking through the user first via culturual analysis.</p>
        <a href="#contact" class="hj-btn btn-red">Get In Touch</a>
     </div>
  </div>
</template>

<script>
export default {
  name: "hero",
  data() {
    return {
      nav: {
        "#about-me": "far fa-user",
        "#experience": "fas fa-suitcase",
        "#projects": "fas fa-project-diagram",
        "#skills": "fas fa-star",
        "#accolades": "fas fa-award",
        "#artwork": "fas fa-palette",
        "#contact": "fas fa-phone"
      }
    }
  }
}
</script>

<style lang="css">
#app #hero {
	background-color: #c11f1e;
	color: #fff
}

#app .main_nav {
	background-color: #000;
	width: 100%;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	padding-top: 30px;
	padding-bottom: 30px;
	padding-right: 0;
	width: 80px
}

#app .main_nav a {
	color: #000;
	font-size: 40px;
	transition: .5s ease-in-out;
	width: 100%;
	display: flex;
	justify-content: center;
	padding: 20px;
	text-align: center;
	text-decoration: none
}

#app .main_nav>a i {
	color: #ffec09;
	transition: .5s ease-in-out
}

#app .main_nav>a:hover i {
	color: #000
}

#app .main_nav>a:hover {
	background-color: #ffec09
}

#app .hero {
	margin: auto 0;
	display: flex;
	width: 100%;
	flex-direction: column;
	padding-left: 30px;
	font-family: Poppins, sans-serif;
	max-width: 1000px
}

#app .hero .h-rule {
	background-color: #fff;
	border: 1px solid;
	content: " ";
	width: 30px;
	vertical-align: super;
	margin-top: 5px
}

#app .hero h1 {
	font-weight: 900;
	text-transform: uppercase;
	font-size: 64px;
	line-height: 1.5
}

#app .hero p {
	max-width: 400px;
	font-weight: 400;
	margin-bottom: 0
}

#app .hero span p {
	text-transform: uppercase;
	font-weight: 600;
	width: auto
}

#hero .hero .h-rule {
	margin-right: 30px
}

@media(max-width:600px) {
	#hero .hero h1 {
		font-size: 32px
	}
}
</style>
