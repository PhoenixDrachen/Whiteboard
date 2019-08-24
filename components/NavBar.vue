<template>
    <div id="NavBar">
        <div class="navbar_wrapper">
            <div class="icon_container active">
                <img src="/Closed-Light.svg" alt="">
            </div>
            <div class="icon_container">
                <img src="/Numbers-Dark.svg" alt="">
            </div>
            <div class="icon_container">
                <img src="/Taks-Dark.svg" alt="">
            </div>
            <div class="icon_container">
                <img src="/Deals-Dark.svg" alt="">
            </div>
            <div class="icon_container">
                <img src="/Launch-Dark.svg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/variables';

.navbar_wrapper{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height:125px;
    .icon_container{
        height:100px;
        padding:10px;
        img{
            width:75px;
        }
        &.active{
            background-color:$dark_base;
            flex-grow: 2;
            border-radius:25px;
        }
    }
}

</style>
