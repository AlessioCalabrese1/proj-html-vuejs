<template>
<footer class="position-relative">
    <FooterElements />
    <div class="copyright">
        CopyrightEverlead@MickadoThemes
    </div>

    <Anchor />
</footer>
  
</template>

<script>
import FooterElements from './FooterElements.vue';
import Anchor from '../Main/Anchor.vue';
export default {
    components: { FooterElements, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

.copyright{
    text-align: center;
    color: $textInfoColor;
    font-weight: lighter;
    font-size: 12px;
    background-color: $textColorHover;
    padding: 10px 0;
}

.anchor{
    right: 20px;
    bottom: 20px;
}
</style>