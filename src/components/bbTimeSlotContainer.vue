<template>
    <section class="timeslot-container--bg">
        <h2 class="timeslot-container--title">Selecteer een tijdsslot</h2>
        <h3 class="timeslot-container--subtitle">Hoelaat wil je ongeveer langskomen?</h3>
        <div class="timeslot-container--wrapper">
            <bb-picker :check="true">
                <bb-time-slot start="09:00" middle="tot" end="10:00"/>
            </bb-picker>
            <bb-picker>
                <bb-time-slot start="10:00" middle="tot" end="11:00"/>
            </bb-picker>
            <bb-picker>
                <bb-time-slot start="11:00" middle="tot" end="12:00"/>
            </bb-picker>
            <bb-picker>
                <bb-time-slot start="12:00" middle="tot" end="13:00"/>
            </bb-picker>
            <bb-picker>
                <bb-time-slot start="13:00" middle="tot" end="14:00"/>
            </bb-picker>
        </div>
        <div class="timeslot-container--scroll">
            <font-awesome-icon icon="arrow-right" />
        </div>
        <bb-primary-button class="timeslot-container--button" txt="Verder" />
    </section>
</template>

<script>
import bbPrimaryButton from './bbPrimaryButton.vue'
import bbPicker from './bbPicker.vue'
import bbTimeSlot from './bbTimeSlot.vue'

export default {
    name: 'bbTimeSlotContainer',
    components: {
        bbPicker, bbTimeSlot, bbPrimaryButton
    }
}
</script>

<style lang="scss" scoped>
$timeslot-bgc-active: #0064FF;
$timeslot-bgc-inactive: #FFFFFF;
$timeslot-check: #05E9B4;
$timeslot-check-color: #FFFFFF;
$timeslot-title: #FFFFFF;
$timeslot-subtitle: #FFFFFF;
$timeslot-scroll: #0064FF;

.timeslot-container {
    &--bg {
        position: relative;
        margin-left: 40px;
        height: 280px;
    }

    &--title {
        font-family: 'Palanquin Bold', sans-serif;
        font-size: 20px;
        color: $timeslot-title;
        margin-bottom: 0;
    }

    &--subtitle {
        font-family: 'Open Sans', sans-serif;
        font-weight: 600;
        font-size: 13px;
        margin: 0;
        color: $timeslot-subtitle;
    }

    &--wrapper {
        height: 150px;
        white-space: nowrap;
        overflow-x: scroll;
        overflow-y: hidden;
    }

    &--button {
        position: absolute;
        bottom: 15px;
        right: 25px;
    }

    &--scroll {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right: 15px;
        bottom: 122px;
        color: white;
        height: 26px;
        width: 26px;
        background-color: $timeslot-scroll;
        border-radius: 50%;
    }
}
</style>
