<template lang="html">
<div id="skills" class="container-fluid mb-5">
   <h3 sec_num="04" class="section-title">Skills</h3>
   <div class="row mt-5">
      <div class="col-12 col-md-3 skill" v-for="(skill, index) in skills" :key="index">
        <img src="" alt="" class="skill-logo">
        <h3 class="skill-name">{{skill}}</h3>
      </div>
   </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        "React",
        "Javascript",
        "Java",
        "Android Studio",
        "Lua",
        "Python",
        "HTML",
        "CSS",
        "Golang",
        "VueJS",
        "NodeJS"
      ]
    }
  }
}
</script>

<style lang="css" scoped>
#skills .skill {
	position: relative;
	border-left: 1px solid grey;
	border-right: 0
}

#skills .skill+#skills .skill,
#skills .skill:last-of-type {
	border-right: 1px solid grey
}

#skills .skill:after {
	background-color: grey;
	width: 155%;
	bottom: 0;
	content: "";
	height: 1px;
	left: 50%;
	position: absolute;
	transform: translateX(-50%)
}

@media(max-width:768px) {
	#skills .skill,
	#skills .skill:last-of-type {
		border-right: 0
	}
}
</style>
