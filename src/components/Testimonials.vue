<template>
    <section>
        <div>
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
section>div {
    width: 90%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
}

.testimonials-container {
    width: 50%;
}
</style>