<template>
    <div id="clients" >
        <div class="cardContainer" v-for="developer in developers" :key="developer.name" >
            <DeveloperClientCard :developer="developer" />
        </div>
    </div>
</template>

<script>
import DeveloperClientCard from '../components/DeveloperClientCard'
export default {
  components: { DeveloperClientCard },
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
