<template>
  <section>
    <div>
        <div class="comunicate-container">
            <div class="row">
                <Maps />

                <div class="col-6">
                    <div>Contact Us<span>.</span></div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    <div class="line"></div>
                    <form>
                        <input type="text" placeholder="Your Name" class="name">
                        <input type="email" placeholder="Your Email" class="email">
                        <input type="text" placeholder="Write a message..." class="w-100 text">
                        <input type="submit">
                    </form>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import Maps from './Maps.vue';
export default {
    components: { Maps }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

section > div{
    width: $widthElement;
    margin: 0 auto;
}

.comunicate-container{
    width: 70%;
    margin: 0 auto;
}

.line{
    border: 1px solid $textColorHover;
    width: 10%;
}

.name{
    margin-right: 15px;
    width: calc(50% - 7.5px);
}
.email{
    width: calc(50% - 7.5px);
}
</style>