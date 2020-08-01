<template lang="html">
  <div class="container row m-5">
     <div class="container col" style="display: flex; justify-content: center; flex-direction: column; text-align: left;">
        <h3 sec_num="01" class="section-title">Who Am I</h3>
        <p>I am Mohammed Ajao, a Software Engineer currently working at Facebook. To develop my projects, I take a humanistic approach and use culture as a lens. My games, web applications, books, hobbies, and my music all take focus on the customer/user experience at the forefront of their work.<br><br>You could call me an anime-loving, rice-addicted gym junkie who currently attends <span class="violet">New York University</span>. If you love anime or modded Minecraft, feel free to contact me as well.</p>
     </div>
     <div class="container col-6 d-none d-lg-flex" style="display: flex; justify-content: center; align-items: center;"><img src="@/assets/profile_pic.ba69fefb.jpg" alt="" class="avatar"></div>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
#about-me {
	display: flex;
	justify-content: center;
	flex-direction: row;
	color: #372c2b
}

#app #about-me .container>div {
	width: 50%
}

#app #about-me img {
	box-shadow: 0 1px 5px rgba(0, 0, 0, .3);
	border-radius: 5px;
	width: 250px;
	height: 250px
}
</style>
