<template>
  <div id="tasks">
    <div v-for="developer in developers" :key="developer.name" class="cardContainer">
      <DeveloperTasksList :developer="developer" />
    </div>
  </div>
</template>

<script>
import DeveloperTasksList from '~/components/DeveloperTasksList'
export default {
  components: { DeveloperTasksList },
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
    #tasks{
        display: flex;
        flex-direction: row;
        margin:20px;
        justify-content:space-between;
        .cardContainer{
            width:calc(33% - 10px);
        }
    }
</style>
