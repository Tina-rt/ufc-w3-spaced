<script>
import Border from './Border.vue';

export default{
    components:{
        Border
    }
}
</script>

<template>
    <div class="suit-section">
        <div class="suit-image">
            <img src="/images/astronaut.png" alt="Astronaut">
        </div>
        <div class="suit-body">
            <div class="suit-header">
                <div class="suit-title-section">
                    <div class="subtitle">E N H A N C E D <span class="mi-2"> </span> L U X U R Y</div>
                    <div class="title">BIO SUIT 2.0</div>
                </div>
                <div class="info-aside">2022 UPGRADE</div>
            </div>
            <Border />
            <div class="suit-p">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis,
                ex. Fugit id voluptatibus est labore reiciendis corporis sit. Temporibus blanditiis aperiam saepe tempore,
                esse a iusto iste? Praesentium, itaque? Voluptatem?
                <div class="suit-desc">
                    <table>
                        <tr>
                            <td>
                                <div class="value">50%</div>
                                <div class="label">LIGHTER</div>
                            </td>
                            <td>
                                <div class="value">HUD</div>
                                <div class="label">CONTROLS</div>
                            </td>
                            <td>
                                <div class="value">8HRS</div>
                                <div class="label">OXYGEN</div>
                            </td>
                        </tr>
                        <tr>
                            <td class="no-border"></td>
                            <td colspan="2" class="">
                                <div class="learn-more-section">

                                    <div class="learn-more">LEARN MORE</div>
                                    <div class="btn-aside">></div>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>

        </div>
    </div>
</template>

<style scoped lang="scss">
.suit-section {
    /* padding: 40px; */
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.suit-image {
    width: 50%;
}

.suit-image img {
    width: 100%;
}

.suit-body {
    padding: 30px;
    width: 40%;
    display: flex;
    flex-direction: column;

}



.suit-header {
    display: flex;
    flex-direction: row;
    align-items: end;
    justify-content: space-between;
}

.suit-title-section {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.info-aside {
    margin: 5px;
}


.suit-p {
    font-family: consolas;
    padding: 20px 0 0 60px;
    width: 70%;
    font-size: 1.2em;
}

.suit-desc {
    width: 100%;
    margin-top: 30px;
    table {
        width: 100%;

        border-collapse: collapse;

        .no-border {
            border: none;
        }

        td {
            border: 1px solid rgba(255, 255, 255, 0.247);
            text-align: center;
            width: 100px;
            height: 100px;

            .value {
                font-size: 2.4em;
                font-weight: bold;
                font-family: 'Bebas';
            }

            .label {}
        }
        .learn-more-section{
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            width: 100%;

            .learn-more{
                width: 100%;
                color: var(--color-btn);
            }

            .btn-aside{
                padding: 40px;
                border-left: 1px solid rgba($color: #fff, $alpha: 0.247);
            }
        }

    }
}</style>