<template>
    <div class="event-card d-flex">
        <div class="date text-center me-3">
            <p class="day">{{ event.day }}</p>
            <p class="month">{{ event.date }}</p>
        </div>

        <div class="info">
            <p class="type mb-3">{{ event.type }}</p>
            <p class="mb-1">
                <i class="fa-regular fa-clock me-2"></i>
                <span>{{ event.time }}</span>
            </p>
            <p class="mb-3">
                <i class="fa-solid fa-location-dot me-2"></i>
                <span>{{ event.location }}</span>
            </p>
            <p class="more">
                Read More
            </p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        event: {
            type: Object,
            require: true
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";

.event-card {
    padding: 25px 30px;
    border-top: 1px solid $eventsMainTextColor;
}
.event-card:hover{
    background-color: white;
    cursor: pointer;
}
.event-card:hover .type{
    color: $textColorHover;
}

.date {
    width: 60px;
    height: 50px;
    background-color: $textColorHover;

    p {
        margin: 0;
        color: white;
    }

    .day{
        font-family: 'Ibarra Real Nova', serif;
        font-weight: bold;
        font-size: 16px;
        margin-top: 5px;
        }

    .month {
        font-size: 12px;
        color: $eventsMainTextColor;
        font-weight: 100;
    }
}

.info {
    position: relative;
    left: 0;
    top: -7px;

    p {
        margin: 0;
        font-size: 12px;
        color: $textInfoColor;
    }

    i {
        color: $textColorHover;
    }

    .type {
        font-weight: bold;
        font-size: 22px;
        color: black;
        font-family: 'Ibarra Real Nova', serif;
    }

    .more {
        color: black;
        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>