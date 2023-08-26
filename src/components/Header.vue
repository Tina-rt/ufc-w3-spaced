<script>
import Logo from './Logo.vue';
export default {
  components: {
    Logo
  }
}
</script>

<template>
  <div class="header">
    <div class="paralax-main">
      <div class="nav">
        <div class="nav-search"><span className="mdi mdi-magnify"></span></div>
        <div class="nav-items">
          <div class="nav-item">DESTINATIONS</div>
          <div class="nav-item">BOOKING</div>
          <div class="nav-item nav-title">
            <Logo />
          </div>
          <div class="nav-item">TECHNOLOGY</div>
          <div class="nav-item">MY TRIPS</div>
        </div>
        <div class="nav-info">
          <span>Weather</span>
          <span class="temp">-50 <sup>c</sup> <i className="mdi mdi-weather-dust"></i> </span>
        </div>
      </div>
      <div class="image-back">
        <img src="/images/bg_mars.jpg" alt="">
      </div>
      <div class="paralax-content">
        <div class="subtitle">THE SAFEST WAY TO</div>
        <div class="title">EXPLORE THE GALAXY</div>

      </div>
      <div class="image-front">
        <img src="/images/front2.png" alt="">
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  height: 100vh;
  width: 100%;
}

.paralax-main {
  position: relative;
  height: 100%;
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
}


.nav {
  position: fixed;
  top: 0;
  width: 100%;
  font-size: 15px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  z-index: 99;
}

.nav::before {
  z-index: -1;
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: #00000005;
  backdrop-filter: blur(20px);
}

.nav-search {
  font-size: 30px;
  padding-left: 10px;
}

.nav-items {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 60%;
}

.nav-title {}

.flip {}

.nav-info {
  display: flex;
  flex-direction: column;
  padding-right: 10px;
}

.nav-info .temp {
  font-size: 25px;
  font-weight: bold;
}

.paralax-content {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: start;
  width: 100%;
  z-index: 2;
  font-size: 3em;
  height: fit-content;
  position: absolute;
  top: 20%;
}

.image-back {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1;
  object-fit: cover;
}

.image-back img {
  height: 100%;
  width: 100%;
}

.image-front {
  z-index: 3;
  position: absolute;
  bottom: 0;
  left: 0;
  /* transform: scale(0.2); */
}

.image-front img {
  width: 100%;
}

.subtitle {
  font-weight: 200;
  font-size: 0.4em;
  word-spacing: 10px;
}

.title {
  font-size: 1.5em;
  font-weight: bold;
}
</style>