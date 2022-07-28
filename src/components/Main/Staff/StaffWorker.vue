<template>
    <div v-show="index === visibleItem" class="staff-container">
        <div class="showcase">
            <img :src="require(`../../../assets/img/${worker.associatedImage}`)" alt="img" class="img-fluid">
        </div>

        <div class="staff-info">
            <h2 class="m-0">{{ worker.name }}</h2>
            <p class="subtitle">{{ worker.workingPosition }}</p>
            <div class="line"></div>
            <p class="info">{{ worker.info }}</p>
            <div class="social-icon-container d-flex">
                <i class="fa-brands fa-linkedin me-2"></i>
                <i class="fa-brands fa-facebook me-2"></i>
                <i class="fa-brands fa-square-twitter"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        worker: {
            type: Object,
            require: true
        },
        index:{
            type: Number,
            require: true
        },
        visibleItem:{
            type: Number,
            require: true
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

    .staff-container{
        width: 70%;
        margin: 0 auto;
        display: flex;
        align-items: center;
    }

    .showcase{
        width: 65%;
    }

    .staff-info{
        width: 65%;
        position: relative;
        top: 50%;
        left: -50px;
        background-color: white;
        padding: 70px 50px ;
    }

    .line{
        border: 1px solid $textColorHover;
        width: 10%;
        margin-bottom: 15px;
    }

    .subtitle{
        font-size: 12px;
        color: $textInfoColor;
    }

    .info{
        color: $textInfoColor;
        font-size: 16px;
    }

    .fa-brands{
        font-size: 18px;
        color: $textColorHover;
    }
    .fa-brands:hover{
        color: black;
        cursor: pointer;
    }

    h2{
        font-family: 'Ibarra Real Nova', serif;
        font-weight: bold;
        font-size: 40px;
    }
</style>