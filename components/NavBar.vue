<template>
    <div id="NavBar">
        <div class="navbar_wrapper">
            <transition-group tag="div">
                <div v-for="icon in icons" :key="icon.name" :class="{'icon_container':true, 'active':(active == icon.name)}">
                    <svg :viewBox="icon.viewBox" :id="icon.id" @click="active = icon.name">
                        <use :xlink:href="'/' + icon.name + '.svg#Layer_2'" />
                    </svg>
                    <span>{{ icon.name }}</span>
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
      icons: [
        { name: 'Closed', viewBox: '0 0 280.49 287.98', id: 'closed' },
        { name: 'Totals', viewBox: '0 0 266.98 266.53', id: 'totals' },
        { name: 'Tasks', viewBox: '0 0 301.84 280.87', id: 'tasks' },
        { name: 'Deals', viewBox: '0 0 368.85 365.06', id: 'deals' },
        { name: 'Launch', viewBox: '0 0 326.05 313.21', id: 'launch' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/variables';

#NavBar{
    height:125px
}
#tasks,
#closed,
#totals,
#launch,
#deals{
    width:75px;
    fill:#1F2421;
}

.navbar_wrapper>div{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height:125px;
    .icon_container{
        height:100px;
        width:100px;
        padding:12px;
        overflow:hidden;
        border-radius:25px;
        position: relative;
        transition:width 1s ease, background-color 1s ease;
        &:hover{
            background-color:#1F2421;
            #tasks,
            #closed,
            #totals,
            #launch,
            #deals{
                fill:#DCE1DE
            }
        }
        span{
            position:absolute;
            opacity: 0;
            top: calc(50% - 24.4px);
            right:-150px;
            transition: right 1s ease;
        }
        &.active{
            background-color:$dark_base;
            width:250px;
            color:$light_base;
            font-size: 40px;
            font-family: 'Roboto';
            padding-right:15px;
            font-weight:700;
            #tasks,
            #closed,
            #totals,
            #launch,
            #deals{
                fill:#DCE1DE
            }
            span{
                right:20px;
                opacity:1
            }
        }
    }
}
</style>
