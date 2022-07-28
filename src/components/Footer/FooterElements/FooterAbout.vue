<template>
  <div class="col-3">
    <ul>
        <li class="title mb-3">
            {{ title }}
            <div class="line mt-3"></div>
        </li>

        <li v-for="(element, index) in elementsList" :key="index" class="info mb-3">
            {{ element }}
        </li>

        <li>
            <i class="fa-brands fa-linkedin"></i>
            <i class="fa-brands fa-facebook"></i>
            <i class="fa-brands fa-square-twitter"></i>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    data: function(){
        return{
            title: "About",
            elementsList:[
                "We have created Everlead to effectly become the stepping stone towards meeting all your goals & achiving business succes."
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

ul{
    list-style: none;
    li{
        
    }
}

.title{
    color: white;
    font-size: 20px;
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
    color: white;
    font-size: 18px;
    margin-right: 8px;
}

</style>