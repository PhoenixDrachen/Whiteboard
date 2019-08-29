<template>
  <div>
    <nav>
      <Totals />
      <div id="NavBar">
        <div class="navbar_wrapper">
            <div v-for="(item, key) of items" :key="key" :class="{'icon_container':true, 'active':(active == item.icon.name)}">
                <nuxt-link :to="item.to" >
                    <svg :viewBox="item.icon.viewBox" :id="item.icon.id" @click="active = item.icon.name">
                        <use :xlink:href="'/' + item.icon.name + '.svg#Layer_2'" />
                    </svg>
                    <span>{{ item.icon.name }}</span>
                </nuxt-link>
            </div>
        </div>
      </div>
      <Goals />
    </nav>
    <nuxt />
  </div>
</template>

<script>
import Totals from '~/components/Totals'
import Goals from '~/components/Goals'
export default {
  components: {
    Totals,
    Goals
  },
  data () {
    return {
      items: [
        {
          title: 'Closed',
          icon: {
            name: 'Closed',
            viewBox: '0 0 280.49 287.98',
            id: 'closed'
          },
          to: { name: 'index' }
        },
        {
          title: 'Totals',
          icon: {
            name: 'Totals',
            viewBox: '0 0 266.98 266.53',
            id: 'totals'
          },
          to: { name: 'totals' }
        },
        {
          title: 'Tasks',
          icon: {
            name: 'Tasks',
            viewBox: '0 0 301.84 280.87',
            id: 'tasks'
          },
          to: { name: 'tasks' }
        },
        {
          title: 'Deals',
          icon: {
            name: 'Deals',
            viewBox: '0 0 368.85 365.06',
            id: 'deals'
          },
          to: { name: 'deals' }
        },
        {
          title: 'Launch',
          icon: {
            name: 'Launch',
            viewBox: '0 0 326.05 313.21',
            id: 'launch'
          },
          to: { name: 'launch' }
        }
      ],
      active: 'Closed'
    }
  }
}
</script>
<style lang="scss">
@import '~/assets/variables';

html{
  background-color:$light_base;
}

nav{
  display:flex;
  flex-direction: row;
  padding:15px;
  #NavBar{
    flex-grow:3;
    height:125px;
    padding-left:10px;
    padding-right:10px;
  }
  #tasks,
  #closed,
  #totals,
  #launch,
  #deals{
      width:75px;
      fill:$dark_base;
      transition: fill .25s ease-out
  }

  .navbar_wrapper{
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
          transition:width 1s ease-out, background-color 1s ease-out;
          &:hover{
              background-color:$dark_base;
              #tasks,
              #closed,
              #totals,
              #launch,
              #deals{
                  fill:$light_base
              }
          }
          span{
              position:absolute;
              opacity: 0;
              top: calc(50% - 24.4px);
              right:-150px;
              transition: right 1s ease-out;
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
                  fill:$light_base
              }
              span{
                  right:20px;
                  color:$light_base;
                  opacity:1
              }
          }
      }
  }
}
</style>
