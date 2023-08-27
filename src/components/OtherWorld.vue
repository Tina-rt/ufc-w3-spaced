<template>
    <div class="other-section">
        <div class="other-header">
            <div class="subtitle">D I S C O V E R</div>
            <div class="title">OTHER WORLDS</div>
        </div>
        <div class="other-body">
            <div class="other-tabs">
                <div class="other-tab">MOON</div>
                <div class="other-tab">MARS</div>
                <div class="other-tab">EUROPA</div>
                <div class="other-tab">TITAN</div>
                <div class="other-tab">SATURN</div>
                <div class="other-tab">NEPTUNE</div>
            </div>
            <div class="other-details">
                <div class="other-article">
                    <div class="other-details-header">
                        <div class="title">THE RED PLANET</div>
                        <div class="trip-delay">3 DAY TRIP</div>
                    </div>
                    <div class="other-p">
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident omnis ut rerum,
                            consequatur reprehenderit ratione laborum rem? Excepturi, incidunt debitis suscipit, quam
                            distinctio voluptas optio natus consectetur placeat reprehenderit possimus!</p>

                    </div>
                </div>
                <div class="other-desc">
                    <table>
                        <tr>
                            <td>
                                <div class="value">38%</div>
                                <div class="label">GRAVITY</div>
                            </td>
                            <td>
                                <div class="value">24HR</div>
                                <div class="label">IN A DAY</div>
                            </td>
                            <td>
                                <div class="value">-69 <sup>F</sup></div>
                                <div class="label">AVG TEMP</div>
                            </td>
                        </tr>
                        <tr class="footer">
                            <td colspan="3" class="">
                                <div class="learn-more-section">

                                    <div class="learn-more">BOOK A TRIP</div>
                                    <div class="btn-aside"> <i className="mdi mdi-chevron-left"></i> </div>
                                    <div class="btn-aside"><i className="mdi mdi-chevron-right"></i></div>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
                <div class="other-img">
                    <img src="/images/mars.png" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.other-section {
    width: 90%;
    margin: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;

    .other-header {
        text-align: center;
    }

    .other-body {
        width: 100%;
        margin: 50px 0;

        .other-tabs {
            display: flex;
            flex-direction: row;
            justify-content: space-evenly;
            flex-wrap: wrap;

            font-weight: 100;
            font-size: 1.1rem;
            padding: 20px;
            border-bottom: 1px solid rgba($color: #fff, $alpha: 0.247);
            .other-tab{
                padding: 10px;
            }
        }

        .other-details {
            margin: 40px 0;
            display: grid;
            grid-template-areas:
                "a b b"
                "c b b";
            @media (max-width: 600px) {
                grid-template-areas:
                "a b"
                "c c";
            }
            width: 100%;

            .other-article {
                width: 700px;
                align-self: end;
                @media (max-width: 600px) {
                    width: auto;
                }
                .other-details-header {
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
                }

                .other-p {
                    font-family: consolas;
                    font-size: 16px;


                }
            }

            .other-desc {
                width: 100%;
                margin-top: 30px;
                grid-area: c;
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

                    .learn-more-section {
                        display: flex;
                        flex-direction: row;
                        justify-content: space-between;
                        align-items: center;
                        width: 100%;

                        .learn-more {
                            width: 100%;
                            color: var(--color-btn);
                        }

                        .btn-aside {
                            padding: 20px;
                            font-size: 40px;
                            height: 100%;
                            border-left: 1px solid rgba($color: #fff, $alpha: 0.247);
                        }
                    }

                    .footer td {
                        height: 70px;
                    }

                }
            }

            .other-img {
                width: 90%;
                padding: 60px;
                grid-area: b;
                img {
                    width: 100%;
                }

                @media (max-width: 600px) {
                    padding: 10px;
                }

            }
        }
    }
}
</style>