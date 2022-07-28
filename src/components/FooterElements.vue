<template>
  <section>
    <div>
        <div class="elements-container">
            <div class="row">
                <FooterAbout />
                <FooterSocial />
                <FooterLinks />
                <FooterContact />
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import FooterAbout from './FooterAbout.vue';
import FooterSocial from './FooterSocial.vue';
import FooterLinks from './FooterLinks.vue';
import FooterContact from './FooterContact.vue';
export default {
    components: { FooterAbout, FooterSocial, FooterLinks, FooterContact }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

section{
    background-color: $backgroundColorFooter;
    padding: 80px 0;
}

section > div{
    width: 90%;
    margin: 0 auto;
}

.elements-container{
    width: 70%;
    margin: 0 auto;
}
</style>