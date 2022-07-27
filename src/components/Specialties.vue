<template>
  <section>
    <h1 class="text-center">Our Specialties<span>.</span></h1>
    <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <div class="line mb-5"></div>
    <div class="specialties-container">
        <div class="row">
            <div class="col-3 text-center" v-for="(specialtie, index) in specialties" :key="index">
                <img :src="require(`../assets/svg/${specialtie.img}`)" alt="img">
                <p class="title">{{ specialtie.title }}</p>
                <p>{{ specialtie.info }}</p>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    data: function(){
        return{
            specialties:[
                {
                    img:"svg-0.svg",
                    title: "Knowing",
                    info: "Lorem ipsum dolor sit amet, quis consect."
                },
                {
                    img:"svg-1.svg",
                    title: "Selling",
                    info: "Lorem ipsum dolor sit amet, quis consect."
                },
                {
                    img:"svg-2.svg",
                    title: "Learning",
                    info: "Lorem ipsum dolor sit amet, quis consect."
                },
                {
                    img:"svg-3.svg",
                    title: "Contact",
                    info: "Lorem ipsum dolor sit amet, quis consect."
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

section{
    width: $widthElement;
    background-color: white;
    margin: 0 auto;
    padding: 50px 0;
}

span{
    color: $textColorHover;
    font-weight: bold;
}
p{
    color: $textInfoColor;
}
.line{
    border: 1px solid $textColorHover;
    width: 3%;
    margin: 0 auto;
}
.specialties-container{
    margin: 0 auto;
    width: 70%;
}
</style>