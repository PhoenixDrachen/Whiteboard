<template>
    <div id="NavBar">
        <div class="navbar_wrapper">
            <div class="icon_container">
                <img src="/Closed-Dark.svg">
                <span v-show="active=='Closed'">Closed</span>
            </div>
            <div class="icon_container active">
                <img src="/Numbers-Light.svg">
                <span v-show="active=='Numbers'">Numbers</span>
            </div>
            <div class="icon_container">
                <img src="/Taks-Dark.svg">
                <span v-show="active=='Tasks'">Tasks</span>
            </div>
            <div class="icon_container">
                <img src="/Deals-Dark.svg">
                <span v-show="active=='Deals'">Deals</span>
            </div>
            <div class="icon_container">
                <img src="/Launch-Dark.svg">
                <span v-show="active=='Launch'">Launch</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return { active: 'Numbers' }
  }
}
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
        overflow:hidden;
        display:flex;
        flex-direction:row;
        align-items:center;
        justify-content: space-between;
        img{
            width:75px;
        }
        &.active{
            background-color:$dark_base;
            flex-grow: 2;
            border-radius:25px;
            color:$light_base;
            font-size: 40px;
            font-family: 'Roboto';
            padding-right:15px;
            font-weight:700;
        }
    }
}

</style>
