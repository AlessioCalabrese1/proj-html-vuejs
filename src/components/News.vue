<template>
  <section>
    <div>
        <h1 class="text-center">Latest News<span>.</span></h1>
        <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum, aperiam!</p>
        <div class="line mb-5"></div>

        <div class="container-fluid d-flex justify-content-between">
            <div>
                <i class="fa-solid fa-arrow-left-long"></i>
            </div>
            
            <div class="events-list">
                <div class="row">
                    <div class="col-4 event-card">
                        <img src="../assets/img/h1-img-03.jpg" alt="" class="img-fluid mb-3">
                        <p class="date mb-1"><i class="fa-regular fa-clock"></i>May, 5 2019 <i class="fa-regular fa-user"></i>Amanda Doe</p>
                        <p class="title mb-2">Next Investment</p>
                        <p class="info mb-3">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem non libero, deleniti...</p>
                        <div class="more">Read More</div>
                    </div>
                </div>
            </div>

            <div>
                <i class="fa-solid fa-arrow-right-long"></i>
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
h1{
    span{
        color: $textColorHover;
    }
}
p.text-center{
    color: $textInfoColor;
}

.line{
    width: 7%;
    border: 1px solid $textColorHover;
    margin: 0 auto;
}

.events-list{
    width: 70%;
}

.event-card{
    padding: 15px;
}

.date{
    font-size: 12px;
    color: $textInfoColor;
    i{
        color: $textColorHover;
    }
}

.title{
    font-weight: bold;
    font-size: 23px;
}
.info{
    color: $textInfoColor;
    font-size: 14px;
}
.more{
    text-transform: uppercase;
    font-weight: bold;
    font-size: 12px;
}
</style>