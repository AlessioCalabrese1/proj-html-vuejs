<template>
    <section>
        <div class="background-title">Testimonials.</div>
        <div class="structure">
            <div>
                <i class="fa-solid fa-arrow-left-long"></i>
            </div>

            <div class="testimonials-container text-center">
                <TestimonialCard v-for="(testimonial, index) in testimonials" :key="index" :testimonial="testimonial" />
            </div>

            <div>
                <i class="fa-solid fa-arrow-right-long"></i>
            </div>
        </div>
    </section>
</template>

<script>
import TestimonialCard from './TestimonialCard.vue';
export default {
    data: function () {
        return {
            testimonials: [
                {
                    img: "h3-img-04.png",
                    name: "Cynthia Clark",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam aperiam voluptates sint impedit, labore molestiae minima eius cupiditate fugiat esse repellendus? Ad, consectetur error!"
                }
            ]
        }

    },

    components: { TestimonialCard }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

section{
    background-color: #181515;
    padding: 80px 0;
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
    top: 0;
    left: 50%;
    transform: translate(-50%, -25%);
    z-index: 1;
}

.testimonials-container {
    width: 40%;
}
i{
    color: white;
}
</style>