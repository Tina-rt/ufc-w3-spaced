<template>
    <div class="plan">
        <div class="plan-header">
            <div class="subtitle">G E T T I N G <span style="margin-left: 10px;"> S T A R T E D</span></div>
            <div class="title">PLAN YOUR TRIP</div>
        </div>
        <div class="plan-body">
            <div class="plan-element">
                <div class="icon">
                    <i className="mdi mdi-racing-helmet"></i>
                </div>
                <div class="plan-title">FIRST TIME</div>
                <div class="plan-content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Veritatis quos corrupti magni rem ullam amet, dignissimos culpa
                    autem laboriosam aperiam fuga aspernatur pariatur eaque recusandae hic ipsa ad ipsam et.
                </div>

            </div>
            <div class="plan-element">
                <div class="icon">
                    <i className="mdi mdi-rocket-launch-outline"></i>
                </div>
                <div class="plan-title">BOOK AND TRIP</div>
                <div class="plan-content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Veritatis quos corrupti magni rem ullam amet, dignissimos culpa
                    autem laboriosam aperiam fuga aspernatur pariatur eaque recusandae hic ipsa ad ipsam et.
                </div>

            </div>
            <div class="plan-element">
                <div class="icon">
                    <i className="mdi mdi-bed-king-outline"></i>
                </div>
                <div class="plan-title">BOOK AND ROOM</div>
                <div class="plan-content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Veritatis quos corrupti magni rem ullam amet, dignissimos culpa
                    autem laboriosam aperiam fuga aspernatur pariatur eaque recusandae hic ipsa ad ipsam et.
                </div>

            </div>

            <div class="plan-element">
                <div class="icon">
                    <i className="mdi mdi-car-side"></i>
                </div>
                <div class="plan-title">FIRST TIME</div>
                <div class="plan-content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Veritatis quos corrupti magni rem ullam amet, dignissimos culpa
                    autem laboriosam aperiam fuga aspernatur pariatur eaque recusandae hic ipsa ad ipsam et.
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.plan {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 100px;
    width: 80%;

    .plan-header {
        text-align: center;
    }

    .plan-body {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 100%;

        margin: 50px 0;

        flex-wrap: wrap;

        .plan-element {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-evenly;
            height: 400px;
            width: 300px;

            .plan-title {
                color: var(--color-btn);
                font-family: 'Bebas';
                font-size: 2em;
            }

            .plan-content{
                text-align: center;
                color: rgba($color: #fff, $alpha: 0.547);
                font-family: consolas;
            }

            .icon {
                font-size: 100px;
                font-weight: 100;
            }
        }
    }
}</style>