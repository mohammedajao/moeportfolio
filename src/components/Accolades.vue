<template lang="html">
  <div class="container">
    <h3 sec_num="05" class="section-title">Awards</h3>
     <h2 class="awards-title">Fruits of Labor</h2>
     <div class="awards-cont">
        <div class="row">
           <div class="col-12 col-md-4 award" v-for="(award, index) in awards" :key="index">
              <h3 class="award-meta">{{award.meta}}</h3>
              <h4 class="award-title">{{award.title}}</h4>
              <p class="award-desc">{{award.desc}}</p>
           </div>
         </div>
     </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      awards: [
        {
          title: "Student Showcase Winner",
          meta: "New York City Science Fair - March 2017",
          desc: "Created a dynamic, object-oriented AI that used the A* algorithm and compared it to a procedurally programmed AI's performance. The data was modeled to show the power of data encapsulation and entity design",
        },
        {
          meta: "GOOGLE INNOVATION CHALLENGE - 2019",
          title: "2nd Place",
          desc: "Designed and pitched with a team of 5 a product, called 6STEP, to help youth easily find communities for their daily problems in six simple steps!"
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
#accolades .award {
	display: flex;
	flex-direction: column
}

#accolades .awards-title {
	font-weight: 800;
	font-size: 60px;
	font-family: Poppins, sans-serif;
	text-transform: uppercase;
	position: relative;
	color: rgba(0, 0, 0, .7)
}

#accolades .award-meta {
	background-color: gold;
	color: #fff;
	padding: 10px;
	font-weight: 800;
	font-size: 10px;
	text-transform: uppercase;
	box-shadow: 0 1px 5px rgba(0, 0, 0, .2)
}

#accolades .award-title[data-v-a2d0ed54]:after {
	content: " ";
	position: absolute;
	bottom: -20px;
	left: 0;
	width: 45px;
	height: 5px;
	background-color: gold
}

#accolades .award-title {
	text-align: right;
	align-self: flex-end;
	margin-bottom: 30px;
	width: 100%;
	font-family: Times New Roman, serif;
	position: relative
}

#accolades .award-desc {
	font-size: 14px
}

</style>
