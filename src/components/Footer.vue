<template>
<footer>
    <FooterElements />
    <div class="copyright">
        CopyrightEverlead@MickadoThemes
    </div>
</footer>
  
</template>

<script>
import FooterElements from './FooterElements.vue';
export default {
    components: { FooterElements }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

.copyright{
    text-align: center;
    color: $textInfoColor;
    font-weight: lighter;
    font-size: 12px;
    background-color: $textColorHover;
    padding: 10px 0;
}
</style>