<template>
<section class="position-relative">
    <img src="../../../assets/img/h1-img-04.jpg" alt="video" class="img-fluid">
    <div><i class="fa-solid fa-play play"></i></div>

    <Anchor />
</section>
  
</template>

<script>
import Anchor from '../Anchor.vue';
export default {
    components: { Anchor }
}
</script>

<style lang="scss" scoped>
    section{
        position: relative;
    }

    .play{
        font-size: 34px;
        color: white;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .anchor{
        right: 20px;
        bottom: 75%;
    }
</style>