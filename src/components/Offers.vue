<script>
import CardOffer from './CardOffer.vue';

export default {
    components: {
        CardOffer
    }
}
</script>
<template>
    <div class="main-offer">
        <div class="offers-header">
            <div class="offer-sub">F E A T U R E S</div>
            <div class="offer-title">ADVENTURES</div>
        </div>
        <div class="offer-list">
            <CardOffer corner="-20%" planet_img="./images/moon.png" image="./images/moon_img.jpg" title="DUNE BUGGY TOUR" subtitle="Moon" price="999"/>
            <CardOffer planet_img="./images/mars.png" image="./images/mars_img.jpg" title="CANYON ADVENTURES" subtitle="Mars" price="1900" />
            <CardOffer planet_img="./images/neptune.png" image="./images/neptune.jpg" title="OCEAN AERIAL TOUR" subtitle="Neptune" price="5000" />
        </div>
    </div>
</template>

<style scoped>
.main-offer {
    font-family: 'Bebas';
    display: flex;
    flex-direction: column;
    align-items: center;
}

.offers-header{
    display: flex;
    flex-direction: column;
    align-items: center;
}
.offer-sub{
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 100;
    font-size: 20px;
}
.offer-title{
    font-size: 3em;
    /* font-weight: bold; */
}

.offer-list{
    margin-top: 40px;
    display: flex;
    flex-direction: row;
}
@media (max-width: 600px) {
    .offer-list{
        flex-direction: column;
    }
}
</style>