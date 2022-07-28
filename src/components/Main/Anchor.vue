<template>
  <a href="#" class="anchor" ><i class="fa-solid fa-arrow-up"></i></a>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

a{
    display: inline-block;
    width: 40px;
    height: 40px;
    background-color: white;
    border-radius: 50%;
    text-align: center;
    line-height: 40px;
    box-shadow: 0px 3px 5px black;
    position: absolute;
    bottom: 0;
    right: -50px;
    i{
        font-size: 20px;
        color: $textColorHover;
    }
}
</style>