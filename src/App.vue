<template>
    <span>
        <bb-header />
        <div class="bb-app-bg">
            <bb-reservation-container />
            <bb-date-picker />
            <bb-time-slot-container />
        </div>
    </span>
</template>

<script>
import bbHeader from './components/bbHeader.vue'
import bbTimeSlotContainer from './components/bbTimeSlotContainer.vue'
import bbReservationContainer from './components/bbReservationContainer.vue'
import bbDatePicker from './components/bbDatePicker.vue'

export default {
    name: 'App',
    components: {
        bbHeader, bbReservationContainer, bbTimeSlotContainer, bbDatePicker
    }
}
</script>

<style>
@font-face {
    font-family: 'Palanquin';
    src: local('Palanquin'),
        url(./fonts/Palanquin/Palanquin-Regular.ttf) format("truetype");
}

@font-face {
    font-family: 'Palanquin Bold';
    src: local('Palanquin'),
        url(./fonts/Palanquin/Palanquin-Bold.ttf) format("truetype");
        font-weight: bold;
}

@font-face {
    font-family: 'Palanquin SemiBold';
    src: local('Palanquin'),
        url(./fonts/Palanquin/Palanquin-SemiBold.ttf) format("truetype");
}

body {
    font-family: 'Palanquin';
}

.bb-app-bg {
    position: absolute;
    top: 178px;
    width: 100%;
    background-image: linear-gradient(to bottom left, #3982FF, #5CD2FF);
    border-top-left-radius: 53px;
}
</style>
