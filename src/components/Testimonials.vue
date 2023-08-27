<script>
import Border from './Border.vue';
import Image from './Image.vue';
export default{
    components:{
        Border,
        Image
    }
}
</script>

<template>
    <div class="testimonial">
        <div class="img-container img1">
            <Image img="./images/test/landscape mountain.jpg" ></Image>
        </div>
        <div class="img-container img2">
            <Image img="./images/spaship.png" ></Image>
        </div>
        <div class="article">
            <div class="article-header">
                <div class="article-title">
                    <div class="subtitle">T E S T I M O N I A L S</div>
                    <div class="title">DOUGLAS QUAID</div>
                </div>
                <div class="aside-btn">
                    <div class="btn"> <i className="mdi mdi-chevron-left"></i> </div>
                    <div class="btn"> <i className="mdi mdi-chevron-right"></i> </div>
                </div>
            </div>
            <Border />
            <div class="article-main">
                <p> <i className="mdi mdi-format-quote-open"></i> Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit porro dolore distinctio sed, 
                    impedit optio, nemo earum quis temporibus magni laborum, consequuntur ipsum accusantium eveniet corporis voluptates minus quisquam nam. <i className="mdi mdi-format-quote-close"></i></p>
            </div>
        </div>
        <div class="img-container img3">
            <Image img="./images/test/base.jpg" />
        </div>
        <div class="img-container img4">
            <Image img="./images/mars_img.jpg" ></Image>
        </div>
        <div class="img-container img5">
            <Image img="./images/test/astronaut.jpg"></Image>
        </div>
    </div>
</template>

<style scoped lang="scss">
.testimonial {

    display: grid;
    grid-template-columns: repeat(2, 1fr) 2fr;
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    width: 80%;

    .img-container img {
        width: 100%;
        // height: 100%;
    }

    .img1 {
        width: 400px;
        align-self: end;
        justify-self: end;
    }

    .img2 {
        // width: 400px;
        height: 500px;
        object-fit: cover;
        align-self: end;
    }

    .img4 {
        // width: 400px;
    }

    .img5 {
        align-self: start;
        justify-self: start;
    }

    .article{
        margin: 50px;
        .article-header{
            display: flex;
            flex-direction: row;
            width: 100%;
            justify-content: space-between;
            align-items: center;

            .aside-btn{
                display: flex;
                flex-direction: row;

                .btn{
                    padding: 20px;
                    font-size: 30px;
                    border: 1px solid rgba($color: #fff, $alpha: 0.247);
                }
            }
        }

        .article-main{
            font-family: consolas;
            word-spacing: 10px;
            font-size: 16px;

            padding: 0 50px;

            i{
                font-size: 40px;
            }
        }
    }
}

@media (max-width: 600px) {
    .testimonial{
        width: 100%;
        grid-template-areas: 
            
            "a b b"
            "a b b"
            "c d d";
        }
        
        .img5{
            grid-area: d;
            align-self: end !important;

        }
        .img1{
            display: none;
        }
        .article{
            grid-area: b;
            margin: 0 !important;
            padding: 0;
            align-items: start !important;
            display: flex;
            flex-direction: column;
            width: auto;
        }
        .img2{
            grid-area: a;
            align-self: start !important;
            width: 100px;
            height: auto !important;
        }
        .img3{
           display: none;
        }
        .img4{
            grid-area: c;
        }
        
}
</style>