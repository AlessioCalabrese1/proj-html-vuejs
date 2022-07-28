<template>
  <div class="col-3">
    <ul>
        <li class="title mb-3">
            {{ title }}
            <div class="line mt-3"></div>
        </li>

        <li class="info mb-2">
            <i class="fa-solid fa-location-dot me-2"></i> 457 BigBlue Street, NY 10013
        </li>

        <li class="info mb-2">
            <i class="fa-solid fa-phone me-2"></i> (315) 5512-2579
        </li>

        <li class="info mb-4">
            <i class="fa-regular fa-envelope me-2"></i> everlead@mickado.com
        </li>

        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Your Name" aria-label="Recipient's username" aria-describedby="button-addon2">
            <button class="btn btn-outline-secondary" type="button" id="button-addon2">Subscribe</button>
        </div>
    </ul>
  </div>
</template>

<script>
export default {
    data: function(){
        return{
            title: "Contact Me",
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

ul{
    list-style: none;
    padding: 0;
}

.title{
    color: white;
    font-size: 23px;
    font-weight: bold;
    font-family: 'Ibarra Real Nova', serif;
}
.line{
    width: 15%;
    border: 1px solid $textColorHover;
}
.info{
    font-size: 14px;
    color: $textInfoColor;
    font-weight: lighter;
}
i{
    color: $textColorHover;
    font-size: 18px;
    margin-right: 8px;
}
a{
    text-decoration: none;
    color: $textInfoColor;
}
.form-control{
    border-radius: 0;
    background-color: $backgroundColorFooter;
    border: 0;
    border-bottom: 1px solid $textInfoColor;
    padding: 0;
    padding-bottom: 5px;
    font-size: 14px;
}
.btn{
    border-radius: 0;
    background-color: $backgroundColorFooter;
    border: 0;
    border-bottom: 1px solid $textInfoColor;
    padding: 0;
    padding-bottom: 5px;
    font-size: 12px;
    font-weight: bold;
    text-transform: uppercase;
    color: white;
}
</style>