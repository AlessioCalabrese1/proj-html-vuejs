<template>
    <div class="col-6 position-relative">
        <img src="../../../assets/img/h1-contact-rev-01.png" alt="maps" class="img-fluid">
        <div class="pointer-structure new-york">
            <img src="../../../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
            <div class="info-box">
                <p class="title">New York Coaching</p>
                <p class="more">Read More</p>
            </div>
        </div>

        <div class="pointer-structure london">
            <img src="../../../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
            <div class="info-box">
                <p class="title">London Coaching</p>
                <p class="more">Read More</p>
            </div>
        </div>

        <div class="pointer-structure melbourne">
            <img src="../../../assets/img/h1-contact-rev-02.png" alt="pointer" class="pointer">
            <div class="info-box">
                <p class="title">Melbourne Coaching</p>
                <p class="more">Read More</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
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
    font-size: 22px;
    font-family: 'Ibarra Real Nova', serif;
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