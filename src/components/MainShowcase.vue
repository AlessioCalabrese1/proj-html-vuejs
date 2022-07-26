<template>
  <section class="position-relative">
    <div class="mainshowcase-slider">
        <img src="../assets/img/rev-slider-main-home-img-03.jpg" alt="slider">
        <img src="../assets/img/rev-slider-main-home-img-02.png" alt="slider" class="d-none">
    </div>

    <div class="mainshowcase-body">
        <div>
            <div class="row">
                <div class="col-1">
                    <i class="fa-solid fa-arrow-left-long"></i>
                </div>

                <div class="col-1"></div>

                <div class="col-4">
                    <div class="mainshowcae-title">
                        Our Team<span>.</span>
                    </div>
                    <div class="mainshowcae-info my-3">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, dolores? Debitis odio veritatis ducimus natus porro blanditiis.
                    </div>
                    <div>
                        <button class="more me-3">
                            <span class="btn-text py-2 px-3">
                                Read More
                            </span>
                            
                            <span class="mx-2">
                                <i class="fa-solid fa-arrow-right-long"></i>
                            </span>
                        </button>

                        <button class="purchase">
                            <span class="btn-text py-2 px-3">
                                Purchase
                            </span>
                            
                            <span class="mx-2">
                                <i class="fa-solid fa-arrow-right-long"></i>
                            </span>
                        </button>
                    </div>
                </div>

                <div class="col-5"></div>

                <div class="col-1 text-end">
                    <i class="fa-solid fa-arrow-right-long"></i>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

    .mainshowcase-slider{
        height: 900px;
        overflow: hidden;
        img{
            position: relative;
            top: -70px;
            left: 0;
        }
    }

    .mainshowcase-body{
        width: $widthElement;
        margin: 0 auto;
        position: absolute;
        left: 50%;
        bottom: 220px;
        transform: translate(-50%, 0);
    }

    .mainshowcase-body > div{
        width: 100%;
    }

    .col-1{
        padding-top: 75px;
    }
    .mainshowcae-title{
        font-size: 75px;
        font-weight: bold;
        span{
            color: $textColorHover;
        }
    }

    .mainshowcae-info{
        color: $textInfoColor;
    }

    .more, .purchase{
        background-color: white;
        border-radius: 0;
        padding: 15px;
        border: 0;
    }

    .purchase{
        background-color: $textColorHover;
        .btn-text{
            color: white;
            border-right: 1px solid white;
        }
        i{
            color: white;
        }
    }

    .btn-text{
        border-right: 1px solid black;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 14px;
    }
</style>