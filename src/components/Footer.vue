<script>
import Logo from './Logo.vue';
export default{
    components:{
        Logo
    }
}
</script>

<template>
    <div class="footer-main">
        <div class="footer-logo">
            <Logo />
        </div>
        <div class="footer-nav">
            <div class="footer-nav-item">DESTINATIONS</div>
            <div class="footer-nav-item">BOOKING</div>
            <div class="footer-nav-item">TECHNOLOGY</div>
            <div class="footer-nav-item">MY TRIP</div>
            <div class="footer-nav-item">FAQ</div>
            <div class="footer-nav-item">SUPPORT</div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.footer-main{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 700px;

    margin-top: 50px;
    background-image: url('/images/footer_bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position-y: center;
    .footer-nav{

        margin: 50px 0;
        display: flex;
        flex-direction: row;
        width: 70%;
        justify-content: space-between;

        flex-wrap: wrap;

        .footer-nav-item{
            padding: 10px;
        }
    }
}
</style>