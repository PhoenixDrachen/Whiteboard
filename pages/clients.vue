<template>
  <div id="clients">
    <div v-for="developer in developers" :key="developer.name" class="cardContainer">
      <DeveloperClientList :developer="developer" />
    </div>
  </div>
</template>

<script>
import DeveloperClientList from '../components/DeveloperClientList'
export default {
  components: { DeveloperClientList },
  data () {
    return {
      developers: [
        {
          name: 'Josh'
        },
        {
          name: 'Jeff'
        },
        {
          name: 'Seth'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
    #clients{
        display: flex;
        flex-direction: row;
        margin:20px;
        justify-content:space-between;
        .cardContainer{
            width:calc(33% - 10px);
        }
    }
</style>
