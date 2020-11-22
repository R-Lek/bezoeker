<template>
    <div class="bgphoto">
        <img class="bgphoto-clip" src="@/assets/bbPhoto.jpg" alt="2 girls with their bikes">
    </div>
</template>

<script>
export default {
    name: 'bbHeader',
}
</script>

<style lang="scss" scoped>
$timeslot-bgc-active: #0064FF;
$timeslot-bgc-inactive: #FFFFFF;
$timeslot-check: #05E9B4;
$timeslot-check-color: #FFFFFF;


.bgphoto {
    z-index: -1;
   
   &-clip {
        width: 320px;
        height: 217px;
    }
}
</style>
