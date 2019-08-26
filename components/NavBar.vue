<template>
    <div id="NavBar">
        <div class="navbar_wrapper">
            <div :class="{'icon_container':true, 'active':(active == 'Closed')}">
                <img v-if="active == 'Closed'" src="/Closed-Light.svg">
                <img v-else src="/Closed-Dark.svg" @click="active='Closed'">
                <span v-if="active=='Closed'">Closed</span>
            </div>
            <div :class="{'icon_container':true, 'active':(active == 'Numbers')}">
                <img v-if="active == 'Numbers'" src="/Numbers-Light.svg">
                <img v-else src="/Numbers-Dark.svg" @click="active='Numbers'">
                <span v-if="active=='Numbers'">Numbers</span>
            </div>
            <div :class="{'icon_container':true, 'active':(active == 'Tasks')}">
                <img v-if="active == 'Tasks'" src="/Tasks-Light.svg">
                <img v-else src="/Taks-Dark.svg" @click="active='Tasks'">
                <span v-if="active=='Tasks'">Tasks</span>
            </div>
            <div :class="{'icon_container':true, 'active':(active == 'Deals')}">
                <img v-if="active == 'Deals'" src="/Deals-Light.svg">
                <img v-else src="/Deals-Dark.svg" @click="active='Deals'">
                <span v-if="active=='Deals'">Deals</span>
            </div>
            <div :class="{'icon_container':true, 'active':(active == 'Launch')}">
                <img v-if="active == 'Launch'" src="/Launch-Light.svg">
                <img v-else src="/Launch-Dark.svg" @click="active='Launch'">
                <span v-if="active=='Launch'">Launch</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return { active: 'Launch' }
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
        flex-grow: 1;
        border-radius:25px;
        transition: flex-grow 2s ease, background-color 2s ease;
        img{
            width:75px;
        }
        &.active{
            background-color:$dark_base;
            flex-grow: 2;
            color:$light_base;
            font-size: 40px;
            font-family: 'Roboto';
            padding-right:15px;
            font-weight:700;
            transition:flex-grow 2s ease, background-color 1s ease
        }
    }
}
</style>
