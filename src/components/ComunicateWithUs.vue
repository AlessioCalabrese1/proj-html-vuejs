<template>
  <section>
    <div>
        <div class="comunicate-container">
            <div class="row">
                <div class="col-6 position-relative">
                    <img src="../assets/img/h1-contact-rev-01.png" alt="maps" class="img-fluid">
                    <div class="pointer-structure new-york">
                        <img src="../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
                        <div class="info-box">
                            <p class="title">New York Coaching</p>
                            <p>Read More</p>
                        </div>
                    </div>

                    <div class="pointer-structure london">
                        <img src="../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
                        <div class="info-box">
                            <p class="title">London Coaching</p>
                            <p class="more">Read More</p>
                        </div>
                    </div>

                    <div class="pointer-structure melbourne">
                        <img src="../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
                        <div class="info-box">
                            <p class="title">Melbourne Coaching</p>
                            <p class="more">Read More</p>
                        </div>
                    </div>
                </div>

                <div class="col-6">

                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {

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

.info-box{
    width: 250px;
    background-color: white;
    padding: 20px;
    display: none;
    box-shadow: 0px 5px 5px black;
    p{
        margin: 0;
    }
}
.new-york{
    position: absolute;
    top: 105px;
    left: 145px;
}
.london{
    position: absolute;
    top: 65px;
    left: 300px;
}
.melbourne{
    position: absolute;
    top: 220px;
    left: 480px;
}
.title{
    font-weight: bold;
    font-size: 20px;
}
.more{
    font-weight: bold;
    text-transform: uppercase;
    font-size: 12px;
}



.pointer:hover{
    cursor: pointer;
}
.pointer:hover + .info-box{
    display: block;
}
.info-box:hover{
    display: block;
}
</style>