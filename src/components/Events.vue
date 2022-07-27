<template>
  <section>
    <div class="events-list">
        <div class="events-container">
            <h3 class="m-0">Upcoming Events</h3>
            <div class="event-card d-flex">
                <div class="date text-center me-3">
                    <p>07</p>
                    <p class="month">Jan, 2022</p>
                </div>

                <div class="info">
                    <p class="type mb-2">Mellbourn Coaching</p>
                    <p class="mb-1">
                        <i class="fa-regular fa-clock me-2"></i>
                        <span>9:00 am - 5:00 pm, Jan 07, 2022</span>
                    </p>
                    <p class="mb-2">
                        <i class="fa-solid fa-location-dot me-2"></i>
                        <span>Cambridge, MA 02138, USA</span>
                    </p>
                    <p class="more">
                        Read More
                    </p>
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

section{
    background-image: url(../assets/img/h1-img-09.jpg);
    height: 1100px;
}

.events-list{
    width: 70%;
    margin: 0 auto;
}
.events-container{
    width: 500px;
    background-color: $backgroundColorMain;
}

h3{
    padding: 25px 30px;
}

.event-card{
    padding: 25px 30px;
}

.date{
    width: 60px;
    height: 50px;
    background-color: $textColorHover;
    p{
        margin: 0;
        color: white;
    }
    .month{
        font-size: 12px;
        color: $eventsMainTextColor;
        font-weight: 100;
    }
}

.info{
    p{
        margin: 0;
        font-size: 12px;
        color: $textInfoColor;
    }
    i{
        color: $textColorHover;
    }
    .type{
        font-weight: bold;
        font-size: 18px;
        color: black;
    }
    .more{
        color: black;
        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>