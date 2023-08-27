<script>
import Header from "./components/Header.vue";
import Booking from "./components/Booking.vue";
import Offers from "./components/Offers.vue";
import Suit from "./components/Suit.vue";
import OtherWorld from "./components/OtherWorld.vue";
import Testimonials from "./components/Testimonials.vue";
import Plan from "./components/Plan.vue";
import Footer from "./components/Footer.vue";

export default{
  components:{
    Header,
    Booking,
    Offers,
    Suit,
    OtherWorld,
    Testimonials,
    Plan,
    Footer
  }
}

</script>

<template>
  <main>
    <Header />
    <Booking />
    <Offers />
    <Suit />
    <OtherWorld />
    <Testimonials />
    <Plan />
    <Footer />
  </main>
</template>

<style scoped>
.border{
  border: 1px solid white;
  position: absolute;
  width: 98%;
  left: 10px;
  top: 100px;
  height: 100vh;
  z-index: 10;
}
main{
  display: flex;
  flex-direction: column;
  align-items: center;
  
}
</style>
