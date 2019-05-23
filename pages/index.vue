<template>
  <div>
    <div id="mainhead" class="slider">
      <h2>
        Video Games:
        <br>A cause for real life violence?
      </h2>
      <nuxt-link to="our-research">OUR RESEARCH</nuxt-link>
      <p>SCROLL</p>
      <img src="arrow.svg" class="bounce" style="width:20px;margin:0 auto;">
    </div>
    <div class="slider second">
      <h3>The Government</h3>
      <img src="government.jpg" class="image">
      <h4>How is the government involved?</h4>
      <nuxt-link to="government">READ MORE ></nuxt-link>
    </div>
    <div class="slider">
      <h3>Parents</h3>
      <img src="parents.jpg" class="image">
      <h4>How are parents to blame?</h4>
      <nuxt-link to="parents">READ MORE ></nuxt-link>
    </div>
    <div class="slider">
      <h3>Video Game Companies</h3>
      <img src="videogamecompanies.jpg" class="image">
      <h4>What are video game companies doing wrong?</h4>
      <nuxt-link to="video-game-companies">READ MORE ></nuxt-link>
    </div>
    <div class="slider last">
      <h3>KIDS</h3>
      <img src="kids.jpg" class="image">
      <h4>How can they be helped?</h4>
      <nuxt-link to="kids">READ MORE ></nuxt-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.slider {
  height: 80vh;
  width: 70%;
  text-align: center;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
}

.slider h2 {
  margin-top: 18vh;
  font-size: 2em;
  margin-bottom: 10vh;
}

.slider a {
  background-color: #2196f3;
  color: white;
  text-decoration: none;
  padding: 15px;
  padding-top: 5px;
  padding-bottom: 5px;
  font-weight: bolder;
  margin-bottom: 15vh;
}

.bounce {
  animation: bounce 3s infinite;
}
@keyframes bounce {
  100% {
    transform: translateY(10px);
  }
  50% {
    transform: translateY(-10px);
  }
  0% {
    transform: translateY(10px);
  }
}

.second {
  margin-top: 20vh;
}

.image {
  width: 100%;
}

.slider h3 {
  margin-bottom: 20px;
}

.slider h4 {
  margin-top: 20px;
  margin-bottom: 20px;
}

.last {
  height: 20vh;
}

.contact {
  margin-top: 250px !important;
  margin-bottom: 0 !important;
}
</style>
