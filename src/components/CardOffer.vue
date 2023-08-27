<script>
export default{
    props:{
        title: "",
        subtitle: "",
        price: 0,
        planet_img: "",
        image: "",
        corner: ""
    }
}
</script>

<template>
    <div class="card" :style="{'background-image': `url(${image})`}">
        <div class="corner-section">
            <div v-if="corner" class="corner">{{ corner }}</div>

        </div>

        <div class="card-body">
            <div class="card-img">
                <img :src="planet_img" :alt="title">
            </div>
            <div class="card-header">
                <div class="card-subtitle">
                    {{subtitle}}
                </div>
                <div class="card-title">
                    {{ title }}
                </div>
            </div>
        </div>
        <div class="card-footer">
            <div class="btn-purchase">FROM ${{ price }}</div>
        </div>
    </div>
</template>

<style scoped lang="scss">

.card {
    opacity: 0.5;
    margin: 50px 40px;
    /* overflow: hidden; */
    position:relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 400px;
    @media (max-width: 600px) {
        width: 300px;
    }
    height: 500px;
    background-size: cover;
    background-position-x: center;
    background-repeat: no-repeat;
    font-size: 20px;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    transition: all 0.4s ease;
}

.card:hover{
    opacity: 1;
}



.corner-section{
    overflow: hidden;
    position: absolute;
    top: 0;
    left: 0;
    width: 100px;
    height: 100px;
}
.corner{
    position: absolute;
    width: 130px;
    height: 42px;
    left: -40px;
    top: 0px;
    background-color: var(--color-btn);
    transform: rotateZ(-48deg);
    font-size: 16px;
    text-align: center;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    /* padding: 10px; */
}
.card-img {
    width: 30%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    transform: translateY(-50%);
}

.card-img img {
    width: 100%;
}

.card-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    height: 50%;
}

.card-header{
    text-align: center;
}

.btn-purchase{
    background-color: var(--color-btn);
    padding: 10px;
    font-weight: bold;
}
</style>