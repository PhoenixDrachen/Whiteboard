<template>
  <div id="Goals">
    <div class="goals_wrapper">
      <div class="goals_month_wrapper">
        <span class="goals_month_header">Monthly Goal:</span>
        <span class="goals_month_amount">${{55*2}}</span>
      </div>
      <div class="goals_week_wrapper">
        <span class="goals_week_header">Weekly Goal:</span>
        <span class="goals_week_amount">${{55*2}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/variables';

.goals_wrapper{
  display:flex;
  flex-direction: column;
  width:400px;
  padding:10px;
  background-color:$light_accent;
  height:125px;
  border-radius:5px;
  box-shadow: 10px 10px 20px rgba(0,0,0,.5);
  justify-content: space-around;
  .goals_month_wrapper, .goals_week_wrapper{
    display:flex;
    flex-direction: row;
    justify-content: space-between;
    span{
      font-family:'Roboto';
      font-weight: 700;
      font-size:32px;
      line-height:38px;
      color:$light_base;
    }
  }
}
</style>
