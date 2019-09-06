<template>
  <div>
    <nav>
      <TheTotals />
      <div id="NavBar">
        <div class="navbar_wrapper">
          <div v-for="(item, key) of items" :key="key" :class="{'icon_container':true, 'active':(active == item.to.name)}">
            <nuxt-link :to="item.to" @click.native="active = item.to.name">
              <svg :id="item.icon.id" :viewBox="item.icon.viewBox">
                <use :xlink:href="'/' + item.icon.name + '.svg#Layer_2'" />
              </svg>
              <span>{{ item.icon.name }}</span>
            </nuxt-link>
          </div>
        </div>
      </div>
      <TheGoals />
    </nav>
    <nuxt />
  </div>
</template>

<script>
import TheTotals from '~/components/TheTotals'
import TheGoals from '~/components/TheGoals'
export default {
  components: {
    TheTotals,
    TheGoals
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
          title: 'Clients',
          icon: {
            name: 'Clients',
            viewBox: '0 0 368.85 365.06',
            id: 'clients'
          },
          to: { name: 'clients' }
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
      active: this.$nuxt.$route.name
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
  #clients{
      width:75px;
      fill:$dark_base;
      transition: fill .25s ease-out, filter .25s ease-out;
      filter: drop-shadow( 3px 3px 2px rgba(31, 36, 33, .7));
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
          border-radius:10px;
          position: relative;
          transition:width .5s .25s ease-out, background-color 1s ease-out;
          &:hover{
              background-color:$dark_base;
              #tasks,
              #closed,
              #totals,
              #launch,
              #clients{
                  fill:$light_base
              }
          }
          span{
              position:absolute;
              opacity: 0;
              top: calc(50% - 30px);
              right:-150px;
              right:20px;
          }
          &.active{
              background-color:$dark_base;
              width:250px;
              color:$light_base;
              font-size: 40px;
              font-family: $body_font;
              padding-right:15px;
              font-weight:700;
              a{
                display:inline-block;
                height:75px;
              }
              #tasks,
              #closed,
              #totals,
              #launch,
              #clients{
                  fill:$light_base;
              }
              span{
                  color:$light_base;
                  opacity:1;
                  transition: opacity .5s .55s ease-out
              }
          }
      }
  }
}
</style>
