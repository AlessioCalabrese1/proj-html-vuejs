<template>
  <div>
    <img :src="require(`../assets/img/${testimonial.img}`)" alt="img">
    <div>
        {{ testimonial.name }}
    </div>

    <div>
        {{ testimonial.info }}
    </div>
  </div>
</template>

<script>
export default {
    props:{
        testimonial:{
            type: Object,
            require: true
        }
    }
}
</script>

<style lang="scss" scoped>

</style>