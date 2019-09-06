<template>
  <div id="launch">
    <LaunchListCard />
    <CheckLaunchListCard />
  </div>
</template>

<script>
import LaunchListCard from '~/components/LaunchListCard'
import CheckLaunchListCard from '~/components/CheckLaunchListCard'
export default {
  components: {
    LaunchListCard,
    CheckLaunchListCard
  }
}
</script>

<style lang="scss" scoped>
    #launch{
        display:flex;
        flex-direction: row;
        margin:20px;
        justify-content:space-between;
        .checkLaunchCard, .launchCard{
            width: calc(50% - 10px);
        }
    }
</style>
