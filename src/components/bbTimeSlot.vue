<template>
    <div class="timeslot-container timeslot-container--active">
        <p>
            <span>
                {{ start }}
            </span>
            <span>
                {{ middle }}
            </span>
            <span>
                {{ end }}
            </span>
        </p>
    </div>
</template>

<script>
export default {
    name: 'bbTimeSlot',
    props: {
        start: String,
        middle: String,
        end: String
    }
}
</script>

<style lang="scss" scoped>
$timeslot-bgc-active: #0064FF;
$timeslot-bgc-inactive: #FFFFFF;
$timeslot-check: #05E9B4;
$timeslot-check-color: #FFFFFF;


.timeslot-container {
    & p {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        padding: 10px;
        color: white;
        font-weight: bold;
    }

    &--inactive {
        background-color: $timeslot-bgc-inactive;
        border-radius: 5px;
        opacity: 25%
    }

    &--active {
        background-color: $timeslot-bgc-active;
        border-radius: 5px;
    }
}
</style>
