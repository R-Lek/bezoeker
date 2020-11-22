<template>
    <section class="reservation-container--bg">
        <h1 class="reservation-container--caption">Reserveer jouw bezoek bij<br>[uw locatie]</h1>
        <h2 class="reservation-container--title">Personen</h2>
        <h3 class="reservation-container--subtitle">Met hoeveel personen kom je?</h3>
        <div class="reservation-container--wrapper">
            <bb-picker>
                <bb-reservation people="1" />
            </bb-picker>
            <bb-picker :check="true">
                <bb-reservation people="2" />
            </bb-picker>
            <bb-picker>
                <bb-reservation people="3" />
            </bb-picker>
            <bb-picker>
                <bb-reservation people="4" />
            </bb-picker>
            <bb-picker>
                <bb-reservation people="5" />
            </bb-picker>
        </div>
        <div class="reservation-container--scroll">
            <font-awesome-icon icon="arrow-right" />
        </div>
    </section>
</template>

<script>
import bbPicker from './bbPicker.vue'
import bbReservation from './bbReservation.vue'

export default {
    name: 'bbReservationContainer',
    components: {
        bbPicker, bbReservation
    }
    
}
</script>

<style lang="scss" scoped>
$reservation-bgc-active: #0064FF;
$reservation-bgc-inactive: #FFFFFF;
$reservation-check: #05E9B4;
$reservation-check-color: #FFFFFF;
$reservation-caption: #FFFFFF;
$reservation-title: #FFFFFF;
$reservation-subtitle: #FFFFFF;
$reservation-scroll: #0064FF;

.reservation-container {
    &--bg {
        margin-left: 40px;
        position: relative;
    }

    &--caption {
        font-family: 'Palanquin Bold', sans-serif;
        font-size: 32px;
        color: $reservation-caption;
    }

    &--title {
        font-family: 'Palanquin Bold', sans-serif;
        font-size: 20px;
        color: $reservation-title;
        margin-bottom: 0;
    }

    &--subtitle {
        font-family: 'Open Sans', sans-serif;
        font-weight: 600;
        font-size: 13px;
        margin: 0;
        color: $reservation-subtitle;
    }

    &--wrapper {
        height: 150px;
        white-space: nowrap;
        overflow-x: scroll;
        overflow-y: hidden;
    }

    &--scroll {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right: 15px;
        bottom: 65px;
        color: white;
        height: 26px;
        width: 26px;
        background-color: $reservation-scroll;
        border-radius: 50%;
    }
}
</style>
