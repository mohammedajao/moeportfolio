<template lang="html">
  <div id="contact" class="container">
    <h3 sec_num="07" class="section-title">Contact</h3>
    <div class="subtitle">Get In Touch</div>
    <div class="contact-info mt-5">
      <a target="_blank" :href="resume" class="hollow-btn resume-link"><div class="overlay"></div>Download Resumé</a>
      <a href="mohammedadrianajao@gmail.com@gmail.com" target="_blank" class="hollow-btn"><span class="overlay"></span>mohammedadrianajao@gmail.com</a>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    resume() {
      return require("@/assets/resume.pdf")
    }
  }
}
</script>

<style lang="css" scoped>
#contact {
	height: 100vh;
	font-family: "Poppins", sans-serif
}

#contact .contact-info {
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column
}

.hollow-btn {
	border: 1px solid grey;
	text-transform: uppercase;
	text-decoration: none;
	transition: .5s ease-in-out;
	color: #000;
	padding: 10px 20px;
	position: relative;
	margin-bottom: 10px
}

.hollow-btn:hover {
	color: #fff
}

.hollow-btn:hover .overlay {
	width: 100%;
	color: #fff;
	background-color: rgba(0, 0, 0, .5)
}

.hollow-btn .overlay {
	content: " ";
	position: absolute;
	background-color: grey;
	left: 0;
	height: 100%;
	width: 0;
	top: 0;
	transition: all .3s;
	z-index: 0;
	background-color: #fff;
	z-index: -1
}

.resume-link {
	font-size: 36px;
	padding: 30px 60px
}

@media(max-width:768px) {
	.resume-link {
		font-size: 24px;
		padding: 10px 20px
	}
}

</style>
