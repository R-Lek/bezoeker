<template>
    <div class="reservation-container reservation-container--inactive">
        <font-awesome-icon class="reservation-container--icon" icon="user" />
        <p>
            {{ people }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'bbReservation',
    props: {
        people: String
    }
}
</script>

<style lang="scss" scoped>
$reservation-bgc-active: #0064FF;
$reservation-border-inactive: #FFFFFF;
$reservation-icon-color: #FFFFFF;

.reservation-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px;

    & p {
        color: white;
        font-weight: bold;
        margin-top: 5px;
    }

    &--inactive {
        border: 1px solid $reservation-border-inactive;
        border-radius: 5px;
    }

    &--active {
        background-color: $reservation-bgc-active;
        border-radius: 5px;
    }

    &--icon {
        margin-top: 15px;
        color: $reservation-icon-color;
    }
}
</style>
