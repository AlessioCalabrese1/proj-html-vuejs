<template>
  <section class="position-relative">
    <div>
        <div class="comunicate-container">
            <div class="row align-items-center">
                <Maps />

                <div class="col-6">
                    <div class="title">Contact Us<span>.</span></div>
                    <p class="info">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    <div class="line"></div>
                    <form>
                        <input type="text" placeholder="Your Name" class="name p-2">
                        <input type="email" placeholder="Your Email" class="email p-2">
                        <textarea name="message" id="message" cols="30" rows="10" placeholder="Write a message..." class="w-100 text px-2"></textarea>

                        <button class="send mt-4">
                                <span class="btn-text py-2 pe-3">
                                    Send
                                </span>

                                <span class="mx-2">
                                    <i class="fa-solid fa-arrow-right-long"></i>
                                </span>
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <Anchor />
  </section>
</template>

<script>
import Maps from './Maps.vue';
import Anchor from '../Anchor.vue';
export default {
    components: { Maps, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

section > div{
    width: $widthElement;
    margin: 0 auto;
    padding: 80px 0;
}

.comunicate-container{
    width: 70%;
    margin: 0 auto;
}

.info{
    font-size: 20px;
}

.title{
    font-size: 50px;
    font-weight: bold;
    span{
        color: $textColorHover;
    }
}

.line{
    border: 1px solid $textColorHover;
    width: 10%;
    margin-bottom: 30px;
}

.name{
    margin-right: 15px;
    width: calc(50% - 7.5px);
}
.email{
    width: calc(50% - 7.5px);
}

.name, .email, .text{
    border: 0;
    border-bottom: 1px solid $textInfoColor;
    background-color: $backgroundColorMain;
}
.text{
    height: 100px;
    margin-top: 20px;
}

.send{
    background-color: $textColorHover;
    padding: 12px 20px;
    border: 0;
    .btn-text {
        color: white;
        border-right: 1px solid white;
        text-transform: uppercase;
        font-size: 14px;
        padding-left: 7px;
    }

    i {
        color: white;
    }
}

.anchor{
    bottom: 97%;
    right: 20px;
}
</style>