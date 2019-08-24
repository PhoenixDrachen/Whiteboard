<template>
  <div>
    <nav>
      <Totals />
      <NavBar />
      <Goals />
    </nav>
  </div>
</template>

<script>
import Totals from '~/components/Totals'
import Goals from '~/components/Goals'
import NavBar from '~/components/NavBar'
export default {
  components: {
    Totals,
    Goals,
    NavBar
  },
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        },
        {
          title: 'Test',
          icon: 'home',
          to: { name: 'test' }
        }
      ]
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
    padding-left:10px;
    padding-right:10px;
  }
}
</style>
