<template>
    <section class="position-relative">
        <StaffWorker v-for="(worker, index) in workers" 
        :key="index"
        :worker="worker"
        :index = "index"
        :visibleItem="visibleItem"/>
        <div class="btn-container d-flex">
            <div @click="goLeft()" class="hov">
                <i class="fa-solid fa-arrow-left-long"></i>
            </div>

            <div @click="goRight()" class="hov">
                <i class="fa-solid fa-arrow-right-long"></i>
            </div>
        </div>

        <img src="../../../assets/svg/svg-4.svg" alt="" class="background-circle">
        <Anchor />
    </section>
</template>

<script>
import StaffWorker from "./StaffWorker.vue";
import Anchor from "../Anchor.vue";
export default {
    data: function () {
        return {
            workers: [
                {
                    associatedImage: "h1-blog-img-04.jpg",
                    name: "Jason Bickford",
                    workingPosition: "Founder and Executive Director",
                    info: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quae sint repellat aperiam doloribus, facilis veniam, fugiat perferendis quod iure dolorem.",
                },
                {
                    associatedImage: "h1-blog-img-01.jpg",
                    name: "Marta Tods",
                    workingPosition: "Manager",
                    info: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quae sint repellat aperiam doloribus, facilis veniam, fugiat perferendis quod iure dolorem.",
                },
                {
                    associatedImage: "h1-blog-img-02.jpg",
                    name: "Jhason Tods",
                    workingPosition: "Marketing",
                    info: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quae sint repellat aperiam doloribus, facilis veniam, fugiat perferendis quod iure dolorem.",
                },
                {
                    associatedImage: "h1-blog-img-03.jpg",
                    name: "Alessio Calabrese",
                    workingPosition: "Sales Clerk",
                    info: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quae sint repellat aperiam doloribus, facilis veniam, fugiat perferendis quod iure dolorem.",
                },
            ],
            visibleItem: 0,
        };
    },
    methods: {
        goRight(){
            if (this.visibleItem == this.workers.length-1) {
                this.visibleItem = 0;
                console.log(this.visibleItem)
            }else{
                this.visibleItem++;
            }
        },

        goLeft(){
            if (this.visibleItem == 0) {
                this.visibleItem = this.workers.length-1;
            }else{
                this.visibleItem--;
            }
        }
    },

    components: { StaffWorker, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

    section{
        width: $widthElement;
        margin: 0 auto;
        padding: 50px 0;
    }

    .btn-container{
        width: 70%;
        margin: 0 auto;
        position: relative;
        z-index: 4;
        top: -54px;
        left: 0;
        div{
            background-color: $textColorHover;
            padding: 15px;
            color: white;
        }
    }

    .anchor{
        bottom: 30px;
    }

    .hov:hover{
        cursor: pointer;
    }

    .background-circle{
        position: absolute;
        top: -70px;
        right: 60px;
        z-index: 1;
    }
</style>