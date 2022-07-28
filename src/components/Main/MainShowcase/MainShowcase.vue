<template>
  <section class="position-relative" id="main_element">
    <MainShowcaseItem v-for="(item, index) in showcaseItems" :key="index" 
    :showcaseItem="item" 
    :visibleItem="visibleItem"
    :direction="direction"
    :index="index" />
    <div class="btn-container d-flex justify-content-between">
        <i class="fa-solid fa-arrow-left-long" @click="goLeft()"></i>
        <i class="fa-solid fa-arrow-right-long text-end" @click="goRight()"></i>
    </div>
  </section>
</template>

<script>
import MainShowcaseItem from "./MainShowcaseItem.vue";
export default {
    data: function(){
        return{
            showcaseItems: [
                {
                    imgInBackground: "rev-slider-main-home-img-03.jpg",
                    title: "Our Team",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, dolores? Debitis odio veritatis ducimus natus porro blanditiis.",
                    btnMore: true,
                    btnPurchase: true,
                },
                {
                    imgInBackground: "rev-slider-main-home-img-02.png",
                    title: "Test",
                    info: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, dolores? Debitis odio veritatis ducimus natus porro blanditiis.",
                    btnMore: true,
                    btnPurchase: false,
                },
            ],
            visibleItem: 0,
            direction: "left",
        }
    },
    methods: {
        goRight(){
            if (this.visibleItem == this.showcaseItems.length-1) {
                this.visibleItem = 0;
            }else{
                this.visibleItem++;
            }
        },

        goLeft(){
            if (this.visibleItem == 0) {
                this.visibleItem = this.showcaseItems.length-1;
            }else{
                this.visibleItem--;
            }
        }
    },

    components: { MainShowcaseItem }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

.btn-container{
    width: $widthElement;
    margin: 0 auto;
    position: absolute;
    top: 65%;
    left: 50%;
    transform: translate(-50%, 0);
}

.btn-container i:hover{
    cursor: pointer;
}
</style>