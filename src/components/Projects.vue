<template lang="html">
  <div class="container">
     <h3 sec_num="03" class="section-title mt-5">My Projects</h3>
     <div class="container">
        <div class="featured-project d-none d-lg-flex row">
           <div class="col-8 featured-img"><img src="https://t3.rbxcdn.com/dbff7027d46e1383105bce86b2d1b0ba"></div>
           <div class="project-info col-4">
              <div class="header">
                 <p class="device-type">IOS | PC | XBox </p>
                 <h3 class="project-title">Bloxxers</h3>
              </div>
              <div class="project-content">
                 <h3>Featured Project</h3>
                 <p>Bloxxers is the first full-fledged brawler game on ROBLOX available on XBOX and PC. Choose from a vast selection of Robloxians and battle your way to the top of the ladder!<br>Recommended for ages 13+</p>
                 <a target="_blank" href="https://www.roblox.com/games/672301689/Bloxxers-Alpha-HIATUS?refPageId=0237c816-e59e-459a-8306-b7179b6d5d11">https://www.roblox.com/games/672301689/Bloxxers-Alpha-HIATUS?refPageId=0237c816-e59e-459a-8306-b7179b6d5d11</a>
              </div>
           </div>
        </div>
        <div class="other-projects mt-5">
           <h3 class="op-title d-none d-lg-block">Other Projects</h3>
           <div class="row">
              <div class="col-12 col-md-6 col-lg-4" v-for="(proj, index) in projects" :key="index">
                 <div class="project-card">
                    <i class="fas fa-folder-open icon"></i><a target="_blank" :href="proj.link" class="link"><i class="fas fa-paperclip" v-if="proj.link"></i></a>
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
          skills: ["ROBLOX Studio", "Lua", "REST"],
        },
        {
          title: "NYU Theta Tau",
          desc: "A website built for NYU Theta Tau I worked on from 2019-Spring 2020. I have worked with a team of brothers inside the fraternity to create a site that represents its values the best. Worked on project roadmaps, designs, code maintenance & best practices, unit tests, user feedback, UX research, browser compatibility, SSR and SEO optimization, bots, automation, and statistical data curation and aggregation to monitor the site's performance.",
          link: "http://www.nyuthetatau.com/",
          skills: ["G-Analytics", "NuxtJS", "Spreadsheets", "REST"]
        },
        {
          title: "Studentern",
          desc: "The site was built to help aid high school students in job opportunities - primarily internships and part-time jobs in local communities while holding a social media network. I managed data migrations, object relations, ORMs, and have developed this project in different frameworks such as Adonis.",
          link: "https://github.com/mohammedajao/studentern",
          skills: ["PHP", "Laravel", "SQL", "VueJS", "REST"]
        },
        {
          title: "Bear Bot",
          desc: "Developed a DiscordJS bot that utilizes several APIs such as YouTube, Spotify, and MAL (MyAnimeList) to serve requested static content. The bot also includes several custom games, a progression system based on text and voice actions, flexible client and role permissions, and utilization of MongoDB to allow users to save data and a currency system. It also includes a RPG in the works.",
          skills: ["Javascript", "Discord.js", "MongoDB", "REST", "Commando Framework"]
        },
        {
          title: "Bloxx Framework",
          desc: "A UI and logic framework aimed at creating 2D platformers for ROBLOX. Features automated and database-compatible cross-platform controller inputs, several cameras for different platforms, a combat system using Raycasting for Hitboxes/Hurtboxes, a mob system, object-oriented classes and custom class instantiation to extend/integrate with the framework, asset loading/preloading, services for Developers/Database/Latency/Physics, several libraries for the aforementioned, API integration with GameAnalytics and Google Spreadsheets, and a RPG library in the works",
          skills: ["Lua", "Javascript", "ROBLOX Studio", "Unit Testing", "REST"]
        },
        {
          title: "FBU Instagram Clone",
          desc: "Features user authentication, profiles, likes, comments, and data persistence in case of network failures. Users can upload images similar to Instagram and edit their profiles.",
          link: "https://github.com/mohammedajao/FBUParstagram",
          skills: ["Android Studio", "Java", "REST", "Parse"]
        },
        {
          title: "FBU Twitter Clone",
          desc: "Users can favourite/like tweets, retweet, compose tweets (along with automatically reply to users), see their feed, see embedded media inside each Tweet with the exception of videos, and see tweets persisted offline and refreshed on every application launc. ",
          link: "https://github.com/mohammedajao/FBUSimpleTweet",
          skills: ["Android Studio", "Java", "REST", "OAUTH", "Twitter API"]
        },
        {
          title: "Memelord",
          desc: "A social media app where users can share memes with others. Users can share memes to other platforms via Android's native share feature, create memes on the app, upload saved memes, like posts, comment on posts, follow users, see trending/latest posts, search for posts, and direct message other users along with seeing live messages via polling with Parse. Only two meme formats are supported on the app currently which are CopyPastas and classic memes with images and text.",
          link: "https://github.com/saclia/memelord",
          skills: ["Android Studio", "Java", "REST", "Parse", "Facebook SDK", "Google SDK", "Photo Editor SDK"]
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
