<template>
    <section>
        <div class="staff-container d-flex">
            <div class="showcase">
                <img src="../assets/img/h1-blog-img-04.jpg" alt="img" class="img-fluid">
            </div>

            <div class="staff-info">
                <h2>Jason Bickford</h2>
                <p class="subtitle">Founder and Executive Director</p>
                <div class="line"></div>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quae sint repellat aperiam doloribus, facilis veniam, fugiat perferendis quod iure dolorem.</p>
                <div class="social-icon-container">

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

    section{
        width: $widthElement;
        margin: 0 auto;
    }

    .staff-container{
        width: 70%;
        margin: 0 auto;
        align-items: center;
    }

    .showcase{
        width: 65%;
    }

    .staff-info{
        width: 60%;
        position: relative;
        top: 50%;
        left: -50px;
        background-color: white;
        padding: 70px 50px ;
    }

    .line{
        border: 1px solid $textColorHover;
        width: 10%;
    }

    .subtitle{
        font-size: 12px;
    }
</style>