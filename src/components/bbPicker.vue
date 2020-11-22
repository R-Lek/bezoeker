<template>
    <div class="picker-container">
        <div :class="check ? 'picker-container--check' : 'picker-container--hide'">
            <font-awesome-icon icon="check" />
        </div>
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'bbPicker',
    props: {
        check: Boolean
    }
}
</script>

<style lang="scss" scoped>
$picker-check: #05E9B4;
$picker-check-color: #FFFFFF;


.picker-container {
    position: relative;
    display: inline-block;
    white-space: normal;
    height: 118px;
    width: 79px;
    border-radius: 5px;
    margin-right: 7px;
    margin-top: 20px;

    &--check {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right: 10px;
        top: -5px;
        height: 26px;
        width: 25px;
        border-radius: 3px;
        background-color: $picker-check;
        color: $picker-check-color;
    }

    &--hide {
        display: none;
    }
}
</style>
