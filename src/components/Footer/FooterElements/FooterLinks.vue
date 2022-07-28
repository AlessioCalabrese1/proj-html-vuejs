<template>
  <div class="col-3">
    <ul>
        <li class="title mb-3">
            {{ title }}
            <div class="line mt-3"></div>
        </li>

        <li v-for="(element, index) in elementsList" :key="index" class="info mb-1">
            <a href="#" @click.prevent="">{{ element }}</a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    data: function(){
        return{
            title: "Important Links",
            elementsList:[
                "About me",
                "About us",
                "Language Packs",
                "Become a coach",
                "Monthly events"
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

ul{
    list-style: none;
    padding: 0;
}

.title{
    color: white;
    font-size: 23px;
    font-weight: bold;
    font-family: 'Ibarra Real Nova', serif;
}
.line{
    width: 15%;
    border: 1px solid $textColorHover;
}
.info{
    font-size: 14px;
    color: $textInfoColor;
    font-weight: lighter;
}
i{
    color: $textColorHover;
    font-size: 18px;
    margin-right: 8px;
}
a{
    text-decoration: none;
    color: $textInfoColor;
}
</style>