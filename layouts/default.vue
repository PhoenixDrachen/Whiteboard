<template>
  <div>
    <div>
      <Totals />
      <NavBar />
      <Goals />
    </div>
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
