<template>
  <section class="position-relative">
    <div>
        <h1 class="text-center font">Latest News<span>.</span></h1>
        <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum, aperiam!</p>
        <div class="line mb-5"></div>

        <div class="container-fluid d-flex justify-content-between align-items-center p-0">
            <div>
                <i class="fa-solid fa-arrow-left-long hov" @click="goLeft()"></i>
            </div>
            
            <div class="events-list">
                <div class="row">
                    <NewsCard v-for="(news, index) in newsList" 
                    :key="index"
                    :news="news"
                    :index="index"
                    :visibleItem="visibleItem" />
                </div>
            </div>

            <div>
                <i class="fa-solid fa-arrow-right-long hov" @click="goRight()"></i>
            </div>
        </div>
    </div>

    <Anchor />
  </section>
</template>

<script>
import NewsCard from './NewsCard.vue';
import Anchor from '../Anchor.vue';
export default {
    data: function(){
        return{
            newsList:[
                {
                    coverImage: "h1-img-03.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Amanda Doe",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
                {
                    coverImage: "h1-img-02.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Amanda Doe",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
                {
                    coverImage: "h1-blog-img-03.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Amanda Doe",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
                {
                    coverImage: "h1-img-07.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Test",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
                {
                    coverImage: "h1-img-08.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Test",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
                {
                    coverImage: "h1-rev-img-01.jpg",
                    publicationDate: "May, 5 2019",
                    author: "Test",
                    title: "Next Investment",
                    description: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...",
                },
            ],
            visibleItem: 0,
        }
    },

    methods: {
        goRight(){
            if (this.visibleItem == this.newsList.length-3) {
                this.visibleItem = 0;
                console.log(this.visibleItem);
            }else{
                this.visibleItem++;
                console.log(this.visibleItem);
            }
        },

        goLeft(){
            if (this.visibleItem == 0) {
                this.visibleItem = this.newsList.length-3;
            }else{
                this.visibleItem--;
            }
        }
    },

    components: { NewsCard, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

section{
    padding: 85px 0;
}

section > div{
    width: $widthElement;
    margin: 0 auto;
}
h1{
    span{
        color: $textColorHover;
    }
}
p.text-center{
    color: $textInfoColor;
}

.line{
    width: 7%;
    border: 1px solid $textColorHover;
    margin: 0 auto;
}

.events-list{
    width: 70%;
}

.hov:hover{
    cursor: pointer;
}
</style>