<template>
    <div class="col-4 event-card" v-show="index >= visibleItem && index <= (visibleItem+2)">
        <img :src="require(`../../../assets/img/${news.coverImage}`)" alt="img" class="img-fluid mb-3">
        <p class="date mb-1"><i class="fa-regular fa-clock pe-1"></i>{{ news.publicationDate }} <i class="fa-regular fa-user px-1"></i>{{
                news.author
        }}</p>
        <p class="title mb-2">{{ news.title }}</p>
        <p class="info mb-3">{{ news.description }}</p>
        <div class="more">Read More</div>
    </div>
</template>

<script>
export default {
    props: {
        news: {
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
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

.event-card {
    padding: 15px;
    position: relative;
    z-index: 2;
}
.event-card:hover {
    cursor: pointer;
}

img{
    height: 261px;
}

.date {
    font-size: 12px;
    color: $textInfoColor;

    i {
        color: $textColorHover;
    }
}

.title {
    font-weight: bold;
    font-size: 30px;
    font-family: 'Ibarra Real Nova', serif;
}

.info {
    color: $textInfoColor;
    font-size: 14px;
}

.more {
    text-transform: uppercase;
    font-weight: bold;
    font-size: 12px;
}
</style>