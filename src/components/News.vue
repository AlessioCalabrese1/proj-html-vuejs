<template>
  <section>
    <div>
        <h1 class="text-center">Latest News<span>.</span></h1>
        <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum, aperiam!</p>
        <div class="line mb-5"></div>

        <div class="container-fluid d-flex justify-content-between align-items-center p-0">
            <div>
                <i class="fa-solid fa-arrow-left-long"></i>
            </div>
            
            <div class="events-list">
                <div class="row">
                    <NewsCard v-for="(news, index) in newsList" 
                    :key="index"
                    :news="news" />
                </div>
            </div>

            <div>
                <i class="fa-solid fa-arrow-right-long"></i>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import NewsCard from './NewsCard.vue';
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
            ]
        }
    },

    components: { NewsCard }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

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

.event-card{
    padding: 15px;
}

.date{
    font-size: 12px;
    color: $textInfoColor;
    i{
        color: $textColorHover;
    }
}

.title{
    font-weight: bold;
    font-size: 23px;
}
.info{
    color: $textInfoColor;
    font-size: 14px;
}
.more{
    text-transform: uppercase;
    font-weight: bold;
    font-size: 12px;
}
</style>