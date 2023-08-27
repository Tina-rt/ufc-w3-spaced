<script>
import Logo from './Logo.vue';
import { gsap } from "gsap";

export default {
  components: {
    Logo
  },
  data() {
    let screenw = window.innerWidth
    return {
      screenw,
      show_nav: screenw > 600
    }
  },
  mounted() {
    window.addEventListener('resize', () => {
      this.screenw = window.innerWidth
    })

    const layers = document.querySelectorAll('.p-layer')

    window.addEventListener('scroll', () => {
      if (window.scrollY < 600) {

        gsap.to('.paralax-content', {
          y: (window.scrollY / 2) + 'px',
          ease: 'ease'
        })
      }
      const nav = document.querySelectorAll('.blur-anim')
      
      if (window.scrollY > 200) {
        gsap.to(nav, {
          '--blur-amount': '10px', // Custom CSS variable for blur amount
          duration: 0.5,           // Animation duration
          onUpdate: () => {
            // Update the pseudo-element's blur using a custom CSS variable
            nav.forEach(element => {
              
              element.style.setProperty('--blur-amount', getComputedStyle(element).getPropertyValue('--blur-amount'));
            });
          },
          
        })
      }
      else{
        nav.forEach(element => {
          element.style.setProperty('--blur-amount', 0)
        })
      }
    })

  }
}
</script>

<template>
  <div class="header">
    <div class="paralax-main">
      <div class="nav blur-anim" :class="{ hide: !show_nav }">
        <div class="nav-search">
          <i className="mdi mdi-window-close" style="float: left;padding: 10px;" @click="show_nav = !show_nav"
            v-if="screenw < 600"></i>
          <span className="mdi mdi-magnify" style="float: right;"></span>
        </div>
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
      <div class="nav-resp blur-anim" v-if="screenw < 600">
        <Logo />
        <div class="menu-btn" @click="show_nav = !show_nav">
          <i className="mdi mdi-menu"></i>
        </div>
      </div>
      <div class="psection">
        <div class="image-back pImage">
          <img src="/images/bg_mars.jpg" alt="">
        </div>
        <div class="paralax-content p-layer" data-speed="1">
          <div class="subtitle">THE SAFEST WAY TO</div>
          <div class="title">EXPLORE THE GALAXY</div>

        </div>
        <div class="image-front pImage" data-speed="1">
          <img src="/images/front2.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
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

.psection {
  position: relative;
  width: 100%;
  height: 100%;
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
  z-index: 199;
}

.nav-resp {
  width: 100%;
  height: 100px;
  z-index: 99;
  position: fixed;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;

  * {
    padding-inline: 20px;
  }

  .menu-btn {
    font-size: 30px;
  }
}

.nav::before,
.nav-resp::before {
  transition: all 0.3s ease;

  z-index: -1;
  content: "";
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: #00000005;
  backdrop-filter: blur(var(--blur-amount));
}



.nav-search {
  font-size: 30px;
  padding-left: 10px;

  @media (max-width:600px) {
    width: 100%;
  }
}

.nav-items {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 60%;
}



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
  text-align: center;
}

.hide {
  display: none;
}

@media (max-width: 600px) {
  .header {
    overflow: hidden;
  }

  .nav-resp {
    margin: 0;
  }

  .nav {

    flex-direction: column;
    align-items: end;
    justify-content: start;
    width: 50%;
    height: 100%;
    margin: 0;
    padding: 0;
    // padding-right: 60px;
    position: fixed;
    right: 0;

    .nav-items {
      flex-direction: column;
      align-items: end;

      .nav-title {
        display: none;
      }

      .nav-item {
        margin: 10px 0;
        padding: 10px;
      }
    }
  }
}
</style>