<template>
    <transition :name="direction">
        <div v-show="visibleItem === index" class="position-relative carousel_item">
            <div class="mainshowcase-slider">
                <img :src="require(`../../../assets/img/${showcaseItem.imgInBackground}`)" alt="slider">
            </div>

            <div class="mainshowcase-body">
                <div class="row">

                    <div class="col-2"></div>

                    <div class="col-4">
                        <div class="mainshowcase-title">
                            {{ showcaseItem.title }}<span>.</span>
                        </div>
                        <div class="mainshowcase-info my-3">
                            {{ showcaseItem.info }}
                        </div>

                        <div class="btn-container">
                            <button class="more me-3" v-if="showcaseItem.btnMore">
                                <span class="btn-text py-2 px-3">
                                    Read More
                                </span>

                                <span class="mx-2">
                                    <i class="fa-solid fa-arrow-right-long"></i>
                                </span>
                            </button>

                            <button class="purchase" v-if="showcaseItem.btnPurchase">
                                <span class="btn-text py-2 px-3">
                                    Purchase
                                </span>

                                <span class="mx-2">
                                    <i class="fa-solid fa-arrow-right-long"></i>
                                </span>
                            </button>
                        </div>
                    </div>

                    <div class="col-6"></div>
                </div>
            </div>
        </div>
    </transition>


</template>

<script>
export default {
    props: {
        showcaseItem: {
            type: Object,
            require: true
        },

        index: {
            type: Number,
            require: true
        },

        visibleItem: {
            type: Number,
            require: true
        },

        direction:{
            type: String,
            require: true
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

.mainshowcase-slider {
    height: 900px;
    overflow: hidden;

    img {
        position: relative;
        top: -70px;
        left: 0;
    }
}

.mainshowcase-body {
    width: $widthElement;
    margin: 0 auto;
    position: absolute;
    left: 50%;
    bottom: 220px;
    transform: translate(-50%, 0);
}

.mainshowcase-body>div {
    width: 100%;
}

.col-1 {
    padding-top: 75px;
}

.mainshowcase-title {
    font-size: 75px;
    font-weight: bold;

    span {
        color: $textColorHover;
    }
}

.mainshowcase-info {
    color: $textInfoColor;
}

.more,
.purchase {
    background-color: white;
    border-radius: 0;
    padding: 15px;
    border: 0;
}

.purchase {
    background-color: $textColorHover;

    .btn-text {
        color: white;
        border-right: 1px solid white;
    }

    i {
        color: white;
    }
}

.btn-text {
    border-right: 1px solid black;
    text-transform: uppercase;
    font-weight: 600;
    font-size: 14px;
}

/* .carousel_item {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.left-enter-active {
    animation: leftInAnimation 0.4s ease-in-out;
}

.left-leave-active {
    animation: leftOutAnimation 0.4s ease-in-out;
}

@keyframes leftInAnimation {
    from {
        transform: translateX(100%);
    }

    to {
        transform: translateX(0%);
    }
}

@keyframes leftOutAnimation {
    from {
        transform: translateX(0%);
    }

    to {
        transform: translateX(-100%);
    }
}

.right-enter-active {
    animation: rightInAnimation 0.4s ease-in-out;
}

.right-leave-active {
    animation: rightOutAnimation 0.4s ease-in-out;
}

@keyframes rightInAnimation {
    from {
        transform: translateX(-100%);
    }

    to {
        transform: translateX(0%);
    }
}

@keyframes rightOutAnimation {
    from {
        transform: translateX(0%);
    }

    to {
        transform: translateX(+100%);
    }
} */
</style>