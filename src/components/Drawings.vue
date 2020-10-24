<template lang="html">
	<div class="container">
		<h3 data-v-5ad8185a="" sec_num="06" class="section-title">Drawings</h3>
		<div class="row container" id="drawings">
			<span v-if="art.length == 0">Loading drawings...</span>
			<!-- <div v-for="(pic, index) in art" :key="index" class="drawing col-md-3 col-4 p-0" :style="{'background-image': 'url('+pic.covers[404]+')'}">

			</div> -->
			<div class="drawing col-md-3 col-4 p-0" v-for="(pic, index) in art" :key="index">
				<img :src="pic.covers[404]" :alt="pic.name" class="drawing">
			</div>
		</div>
	</div>
</template>

<script>
import $ from 'jquery'

export default {
	data() {
		return {
			art: []
		}
	},
	created() {
		// const drawings = document.getElementById("drawings");
		$.getJSON("https://www.behance.net/v2/users/ajaomohamm7597/projects?api_key=1X2hR4X7WmiT7h0S2j5r6qL9eLrkJL87&callback=?").then(data => {
			console.log(data)
			data.projects.map(proj => {
				// let img = document.createElement("img")
				// img.src = proj.covers[404]
				// img.classlist = "drawing"
				console.log(proj)
				// drawings.append(img)
				this.art.push(proj)
			})
		})
	}
}
</script>

<style lang="css" scoped>

/* #drawings .drawing {
	width: 100%;
	height: auto!important;
	padding-top: 100%;
	object-fit: cover;
	background-size: cover;
	overflow: hidden;
	display: inline-block;
} */

#drawings .drawing img{
	width: 100%;
	height: auto;
	overflow: hidden;
}
</style>
