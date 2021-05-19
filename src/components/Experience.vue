<template lang="html">
<div>
  <div class="container pt-5 pl-5">
     <h3 sec_num="02" class="section-title">Work Experience</h3>
     <div class="vert-carousel d-none d-lg-flex d-none d-lg-block">
        <div d class="container logo-cont d-flex"><img :src="jobs[currentSlide].logo" alt=""></div>
        <div id="carousel" class="container slider">
          <div v-for="(job, index) in jobs" :key="index" :id="'wes' + index" :class="currentSlide == index ? 'current_slide' : 'slide'" @click="onJobClick(index)">
            <div class="col-6 d-inline-flex">
               <div class="date">{{job.date}}</div>
               <div class="technologies" style="position: absolute; bottom: 5px; color: rgb(86, 166, 154);" v-if="currentSlide == index">Technologies: </div>
            </div>
            <div class="meta-data col-6">
               <div class="position">{{job.title}}</div>
               <div class="misc" v-if="currentSlide == index">
                  <ul>
                     <li style="position: relative;" v-for="(desc, bulletIndex) in job.bullets" :key="bulletIndex">
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.5em" height="0.8em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 864 1024" style="transform: rotate(360deg);">
                           <path d="M65 65l735 447L64 959zm0-64Q48 1 34 9Q1 28 1 65L0 959q0 37 33 56q7 4 15 6t16 2q9 0 17.5-2.5T97 1013l737-447q30-18 30-54q0-11-3.5-21.5t-10.5-19t-16-13.5L98 11q-5-3-10.5-5t-11-3.5T65 1z" fill="#4AA89B"></path>
                        </svg>
                        {{desc}}
                     </li>
                  </ul>
                  <div class="skills_used" style="color: rgb(86, 166, 154); position: absolute; bottom: 5px; font-size: 14px;">
                    <span v-for="(skill, skillIndex) in job.technologies" :key="skillIndex">{{skill}}<span v-if="skillIndex != job.technologies.length - 1">,&nbsp;</span></span>
                  </div>
               </div>
            </div>
          </div>

        </div>
     </div>
     <div class="d-block d-lg-none">
       <div class="row">
          <div class="col-6 mobile-position" v-for="(job, index) in jobs" :key="index">
             <h3>{{job.date}}</h3>
             <p class="company">{{job.company}}</p>
             <p>{{job.title}}</p>
          </div>
       </div>
     </div>
  </div>
</div>
</template>

<script>
import $ from 'jquery'

export default {
  data() {
    return {
      currentSlide: 0,
      currentLogo: "https://ga-core.s3.amazonaws.com/cms/files/files/000/002/174/original/AllStarCode.png",
      jobs: [
        {
          logo: "https://ga-core.s3.amazonaws.com/cms/files/files/000/002/174/original/AllStarCode.png",
          company: "All Star Code",
          date: "January 2018",
          title: "Curriculum Aide",
          bullets: ["Created Computer Science assignments for students to use as material over the Summer for over 100 students", "Participated in the design of the course for the following Summer"],
          technologies: ["Javascript", "HTML5", "CSS", "SQL"]
        },
        {
          logo: "https://ga-core.s3.amazonaws.com/cms/files/files/000/002/174/original/AllStarCode.png",
          company: "All Star Code",
          date: "June 2018",
          title: "Teaching Assistant",
          bullets: ["Taught over 20 high school students, with a team of 4, basic Computer Science skills such as Data Structures & Algorithms", "Taught soft skills for the workspace and best practices", "Helped students display their pitches and products to a panel of employees at Oath"],
          technologies: ["Firebase", "Javscript"]
        },
        {
          logo: "https://s18798.pcdn.co/vip/wp-content/uploads/sites/7678/2017/11/U%E2%80%A2START-VIP-768x316.png",
          company: "U•Start",
          date: "December 2018",
          title: "U•Start Backend Developer",
          bullets: ["Developed a highly scalable Golang REST API with MongoDB integration", "Worked with graduate students on scalable designs for a microservice architecture while moving from a monolitihic one", "Worked with controllers and middleware for authentication systems"],
          technologies: ["Golang", "MongoDB", "Github"]
        },
        {
          logo: "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/BuzzFeed.svg/1280px-BuzzFeed.svg.png",
          company: "BuzzFeed",
          date: "June 2019",
          title: "Data Infrastructure Intern",
          bullets: ["Developed highly resilient geo-enrichment service handling over 800k messages daily", "Architected servide to pipe data to other downstream services with concurrency and throttling", "Involved in BuzzFeed HackWeek & Intern event-planning"],
          technologies: ["Golang", "AWS", "Git", "Docker"]
        },
        {
          logo: "https://cdn0.tnwcdn.com/wp-content/blogs.dir/1/files/2015/07/sdffdsafsdf-1200x604.png",
          company: "Facebook",
          date: "June 2020",
          title: "Android Developer",
          bullets: ["Developed over seven projects featuring feature-rich apps such as a Twitter or Instagram clone with fail-safe features", "Developed a social media app named Memelord with several social media features, well-developed models, and presented it", "Introduced complex relations such as following, profiles, user instant messaging, and a trending algorithm"],
          technologies: ["Java", "Git", "Android Studio", "Parse", "SQLite", "Room"]
        },
        {
          logo: "https://cdn0.tnwcdn.com/wp-content/blogs.dir/1/files/2015/07/sdffdsafsdf-1200x604.png",
          company: "Facebook",
          date: "June 2021",
          title: "Seller Expansion Android Developer",
          bullets: ["Currently working"],
          technologies: ["Java", "Git", "Android Studio"]
        }
      ]
    }
  },
  methods: {
    onJobClick: function(index) {
      let oldSlide = this.currentSlide
      let pixelMargin = 100;
      this.currentSlide = index;
      if((index - oldSlide) <= 0) {
        pixelMargin = 10;
      }
      $("#carousel").animate({scrollTop: pixelMargin*index}, 500);
    }
  }
}
</script>

<style lang="css" scoped>
#app #experience {
	background-color: #f8f9fb;
}

.vert-carousel {
	margin-bottom: 20px;
	max-height: 400px
}

.vert-carousel #carousel {
	overflow-y: scroll;
	-ms-overflow-style: none
}

.vert-carousel #carousel::-webkit-scrollbar {
	display: none
}

.vert-carousel> {
	transition: .5s ease-in-out
}

.vert-carousel img {
	max-width: 200px
}

.vert-carousel .logo-cont {
	max-width: 300px;
	align-items: center;
	justify-content: center
}

.slider .slide {
	padding-bottom: 10px;
	padding-top: 10px;
	cursor: pointer;
	border-left: 1px solid rgba(0, 0, 0, .1)
}

.slider .slide .date {
	display: inline-block;
	font-family: "Poppins", sans-serif;
	font-size: 18px;
	font-weight: 400;
	margin-right: 20%
}

.slider .slide .meta-data {
	display: inline-block;
	font-family: "Poppins", sans-serif;
	font-size: 16px;
	font-weight: 200;
	opacity: .5
}

.slider .current_slide {
	border-top: 1px solid rgba(0, 0, 0, .1);
	border-bottom: 1px solid rgba(0, 0, 0, .1);
	display: flex;
	flex-direction: row;
	justify-content: space-between
}

.slider .current_slide .meta-data {
	display: inline-block;
	align-self: flex-end;
	height: 100%;
	align-self: flex-start
}

.slider .current_slide .date {
	font-size: 32px;
	display: inline;
	max-width: 100%;
	justify-content: center;
	margin: 30px 0;
	color: #355baf
}

.slider .current_slide .meta-data .position {
	display: inline-block;
	font-size: 28px;
	font-family: "Poppins", sans-serif;
	font-weight: 800;
	color: rgba(0, 0, 0, .5)
}

.slider .current_slide .meta-data .misc ul {
	padding: 10px;
	list-style: none
}

.slider .current_slide .meta-data .misc ul li {
	margin-bottom: 10px;
	font-size: 12px
}

.slider .current_slide .meta-data .misc ul li svg {
	position: absolute;
	left: -10px;
	color: #4aa89b;
	margin-top: 3px
}

.slider .current_slide .col-6:first-of-type {
	justify-content: center;
	align-items: center;
	flex-direction: column;
	align-items: flex-start
}

#experience {
	padding-bottom: 50px
}

#experience .mobile-position h3 {
	font-family: "Poppins", sans-serif;
	color: #000;
	font-weight: 600;
	font-size: 14px
}

#experience .mobile-position p {
	font-size: 16px;
	font-weight: 200;
	opacity: .5
}

#experience .mobile-position .company {
	font-weight: 600;
	margin-bottom: 5px
}

</style>
