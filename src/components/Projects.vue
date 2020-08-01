<template lang="html">
  <div class="container-fluid">
     <h3 sec_num="03" class="section-title mt-5">My Projects</h3>
     <div class="container">
        <div class="featured-project d-none d-lg-flex row">
           <div class="col-8 featured-img"><img src="https://t1.rbxcdn.com/cc44b3fbc7b154103199fa90f5b3ded7"></div>
           <div class="project-info col-4">
              <div class="header">
                 <p class="device-type">IOS | PC | XBox </p>
                 <h3 class="project-title">Bloxxers</h3>
              </div>
              <div class="project-content">
                 <h3>Featured Project</h3>
                 <p>Bloxxers is a and the first full-fledged brawler game on ROBLOX available on XBOX and PC. Choose from a vast selection of Robloxians and battle your way to the top of the ladder!<br>Recommended for ages 13+</p>
                 <a target="_blank" href="https://www.roblox.com/games/672301689/Bloxxers-Alpha-HIATUS?refPageId=0237c816-e59e-459a-8306-b7179b6d5d11">https://www.roblox.com/games/672301689/Bloxxers-Alpha-HIATUS?refPageId=0237c816-e59e-459a-8306-b7179b6d5d11</a>
              </div>
           </div>
        </div>
        <div class="other-projects mt-5">
           <h3 class="op-title d-none d-lg-block">Other Projects</h3>
           <div class="row">
              <div class="col-12 col-md-6 col-lg-4" v-for="(proj, index) in projects" :key="index">
                 <div class="project-card">
                    <i class="fas fa-folder-open icon" v-if="proj.link"></i><a target="_blank" :href="proj.link" class="link"><i class="fas fa-paperclip"></i></a>
                    <h3>{{proj.title}}</h3>
                    <p>{{proj.desc}}</p>
                    <div class="footer row"><span class="sub-skill mr-3" v-for="(skill, skillIndex) in proj.skills" :key="skillIndex">{{skill}}</span></div>
                 </div>
              </div>
           </div>
        </div>
        <a target="_blank" href="https://github.com/mohammedajao" class="hj-btn btn-red mt-5">Explore More</a>
     </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Bloxxers Alpha",
          desc: "The initial release of Bloxxers before it hit Alpha. It utilizes a custom-made API and library with an autonomous database update system, a custom animation system for both GUIS and 3D models, and much more functionality built for the game via modularization of key components. Feel free to ask for the code if you are a recruiter!",
          link: "https://www.roblox.com/games/672301689/Bloxxers-Alpha-HIATUS?refPageId=0237c816-e59e-459a-8306-b7179b6d5d11",
          skills: ["ROBLOX Studio", "Lua"],
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
#projects .featured-project {
	position: relative
}

#projects .featured-img img {
	border-radius: 5px;
	width: 100%;
	box-shadow: 0 1px 5px rgba(0, 0, 0, .2)
}

#projects .project-info {
	display: flex;
	flex-direction: column;
	font-family: Poppins, sans-serif
}

#projects .project-info .header {
	display: flex;
	flex-direction: row;
	justify-content: space-between
}

#projects .project-info .device-type {
	font-weight: 600;
	color: pink;
	display: inline-block;
	vertical-align: middle;
	line-height: 2.3
}

#projects .project-info h3 {
	font-weight: 600;
	display: inline-block
}

#projects .project-content {
	background-color: rgba(50, 50, 50, .3);
	border-radius: 5px;
	margin-left: -100%;
	padding: 25px;
	color: #fff;
	box-shadow: 0 1px 5px rgba(0, 0, 0, .2);
	width: 220%
}

#projects .project-content p {
	font-weight: 400
}

#projects .project-content h3 {
	font-weight: 600;
	color: #0ff
}

#projects .project-content a {
	font-size: 10px;
	text-decoration: none;
	color: #0ff;
	font-weight: 600
}

#projects .other-projects .op-title {
	text-align: center;
	font-weight: 600;
	font-family: Poppins, sans-serif;
	text-transform: uppercase
}

#projects .other-projects .project-card {
	box-shadow: 0 1px 5px rgba(0, 0, 0, .2);
	padding: 20px;
	border-radius: 5px;
	font-family: Poppins, sans-serif;
	min-height: 300px;
	display: flex;
	flex-direction: column;
	overflow: hidden;
	margin-bottom: 10px
}

#projects .other-projects .project-card p::-webkit-scrollbar {
	display: none
}

#projects .other-projects .project-card p {
	-ms-overflow-style: none
}

#projects .other-projects .project-card i.icon {
	font-size: 48px;
	margin-bottom: 10px
}

#projects .other-projects .project-card p {
	font-weight: 400;
	font-size: 12px;
	max-height: 150px;
	overflow-y: scroll
}

#projects .other-projects .project-card .footer {
	bottom: 15px;
	overflow: hidden;
	padding: 10px
}

#projects .other-projects .project-card .sub-skill {
	font-weight: 400
}

#projects .other-projects .project-card h3 {
	font-weight: 600;
	font-size: 24px;
	margin-bottom: 10px
}

#projects .other-projects .project-card .link {
	font-size: 24px;
	position: absolute;
	top: 10px;
	right: 25px;
	text-decoration: none;
	color: #000
}
</style>
