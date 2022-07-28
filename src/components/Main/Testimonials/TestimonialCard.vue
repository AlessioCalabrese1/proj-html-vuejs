<template>
  <div>
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
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

.name{
    color: white;
    font-weight: bold;
    font-size: 20px;
}

.info{
    color: $textInfoColor;
    font-size: 18px;
}
</style>