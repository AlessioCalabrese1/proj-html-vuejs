<template>
  <div v-show="index === visibleItem">
    <img :src="require(`../../../assets/img/${testimonial.img}`)" alt="img" class="mb-3">
    <div class="name mb-3">
        {{ testimonial.name }}
    </div>

    <div class="info mb-3">
        "{{ testimonial.info }}"
    </div>
  </div>
</template>

<script>
export default {
    props:{
        testimonial:{
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

.name{
    color: white;
    font-weight: bold;
    font-size: 20px;
    font-family: 'Ibarra Real Nova', serif;
}

.info{
    color: $textInfoColor;
    font-size: 18px;
}
</style>