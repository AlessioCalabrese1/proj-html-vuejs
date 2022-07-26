<template>
  <section>
    <div class="mainshowcase-slider">
        <img src="../assets/img/rev-slider-main-home-img-03.jpg" alt="slider">
        <img src="../assets/img/rev-slider-main-home-img-02.png" alt="slider" class="d-none">
    </div>

    <div class="mainshowcase-body">
        <div class="container">
            <div class="row">
                <div class="col-1">
                    <i class="fa-solid fa-arrow-left-long"></i>
                </div>

                <div class="col-1"></div>

                <div class="col-4">
                    hello
                </div>

                <div class="col-5"></div>

                <div class="col-1">
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
    }
</style>