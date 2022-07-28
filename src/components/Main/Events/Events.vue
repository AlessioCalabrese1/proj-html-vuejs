<template>
    <section class="position-relative">
        <div class="events-list">
            <div>
                <div class="events-container">
                    <h3 class="m-0">Upcoming Events</h3>
                    <EventsCard v-for="(event, index) in events" :key="index" :event="event" />
                </div>
            </div>
            <Anchor />
        </div>
    </section>
</template>

<script>
import EventsCard from './EventsCard.vue';
import Anchor from '../Anchor.vue';
export default {
    data: function () {
        return {
            events: [
                {
                    day: "07",
                    date: "Jan, 2022",
                    type: "Mellbourn Coaching",
                    time: "9:00 am - 5:00 pm, Jan 07, 2022",
                    location: "Cambridge, MA 02138, USA",
                },
                {
                    day: "11",
                    date: "Jan, 2022",
                    type: "New York Coaching",
                    time: "9:00 am - 5:00 pm, Jan 11, 2022",
                    location: "Cambridge, MA 02138, USA",
                },
                {
                    day: "21",
                    date: "Jan, 2022",
                    type: "London Coaching",
                    time: "9:00 am - 5:00 pm, Jan 21, 2022",
                    location: "Cambridge, MA 02138, USA",
                },
            ]
        }
    },

    components: { EventsCard, Anchor }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

section {
    background-image: url(../../../assets/img/h1-img-09.jpg);
    height: 1100px;
    display: flex;
    align-items: center;
}

.events-list {
    width: 90%;
    margin: 0 auto;
}

.events-list>div {
    width: 70%;
    margin: 0 auto;
}

.events-container {
    width: 500px;
    background-color: $backgroundColorMain;
}

h3 {
    padding: 25px 30px;
    /*     box-shadow: 5px 15px 5px $backgroundColorMain; */
}

.anchor{
    right: 20px;
    bottom: 50%;
    transform: translate(-50%, 0);
}
</style>