<template>
    <div id="NavBar">
        <div class="navbar_wrapper">
            <transition-group tag="div">
                <div v-for="icon in icons" :key="icon" :class="{'icon_container':true, 'active':(active == icon)}">
                    <img v-if="active == icon" :src="'/'+ icon + '-Light.svg'">
                    <img v-else :src="'/'+ icon + '-Dark.svg'" @click="active = icon">
                    <span>{{ icon }}</span>
                </div>
            </transition-group>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      active: 'Launch',
      icons: ['Closed', 'Totals', 'Tasks', 'Deals', 'Launch']
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/variables';

.navbar_wrapper>div{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height:125px;
    .icon_container{
        height:100px;
        width:85px;
        padding:10px;
        overflow:hidden;
        display:flex;
        flex-direction:row;
        align-items:center;
        justify-content: space-between;
        border-radius:25px;
        transition:width 1s ease, background-color .5s ease;
        img{
            width:75px;
            margin-right:10px
        }
        span{
            visibility: hidden;
        }
        &.active{
            background-color:$dark_base;
            width:250px;
            color:$light_base;
            font-size: 40px;
            font-family: 'Roboto';
            padding-right:15px;
            font-weight:700;
            // span{
            //     visibility: visible;
            // }
        }
    }
}
</style>
