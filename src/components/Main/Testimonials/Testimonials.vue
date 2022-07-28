<template>
    <section class="position-relative">
        <div class="background-title">Testimonials.</div>
        <div class="structure">
            <div>
                <i class="fa-solid fa-arrow-left-long" @click="goLeft()"></i>
            </div>

            <div class="testimonials-container text-center">
                <TestimonialCard v-for="(testimonial, index) in testimonials" 
                :key="index" 
                :testimonial="testimonial"
                :index="index" 
                :visibleItem="visibleItem"/>
            </div>

            <div>
                <i class="fa-solid fa-arrow-right-long" @click="goRight()"></i>
            </div>
        </div>

        <Anchor />
    </section>
</template>

<script>
import TestimonialCard from './TestimonialCard.vue';
import Anchor from '../Anchor.vue';
export default {
    data: function () {
        return {
            testimonials: [
                {
                    img: "h3-img-04.png",
                    name: "Cynthia Clark",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aperiam voluptates sint impedit, labore molestiae minima eius cupiditate fugiat esse repellendus? Ad, consectetur error!"
                },
                {
                    img: "h3-img-07.png",
                    name: "Cinzia Nunzia",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aperiam voluptates sint impedit, labore molestiae minima eius cupiditate fugiat esse repellendus? Ad, consectetur error!"
                },
                {
                    img: "h3-img-08.png",
                    name: "Giovanna Olivetti",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aperiam voluptates sint impedit, labore molestiae minima eius cupiditate fugiat esse repellendus? Ad, consectetur error!"
                },
            ],
            visibleItem: 0,
        }
    },
    methods:{
        goRight(){
            if (this.visibleItem == this.testimonials.length-1) {
                this.visibleItem = 0;
            }else{
                this.visibleItem++;
            }
        },

        goLeft(){
            if (this.visibleItem == 0) {
                this.visibleItem = this.testimonials.length-1;
            }else{
                this.visibleItem--;
            }
        }
    },

    components: { TestimonialCard, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

section{
    background-color: #181515;
    padding: 150px 0;
    position: relative;
}

section > div {
    width: $widthElement;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.structure{
    position: relative;
    z-index: 2;
}

.background-title{
    font-size: 300px;
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translate(-50%, -25%);
    z-index: 1;
    font-family: 'Ibarra Real Nova', serif;
    font-weight: bold;
}

.testimonials-container {
    width: 40%;
}
i{
    color: white;
}

.anchor{
    right: 20px;
    bottom: 75%;

}
</style>