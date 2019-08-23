<template>
  <div>
    <div class="totals_wrapper">
      <div class="totals_month_wrapper">
        <span class="totals_month_header">Month To Date:</span>
        <span class="totals_month_amount">${{55*2}}</span>
      </div>
      <div class="totals_year_wrapper">
        <span class="totals_year_header">Year To Date:</span>
        <span class="totals_year_amount">${{55*2}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.totals_wrapper{
  display:flex;
  flex-direction: column;
  width:460px;
  position:absolute;
  top:15px;
  left:15px;
  padding:10px;
  background-color:#6DB57F;
  height:150px;
  border-radius:5px;
  box-shadow: 10px 10px 20px rgba(0,0,0,.5);
  justify-content: space-around;
  .totals_month_wrapper, .totals_year_wrapper{
    display:flex;
    flex-direction: row;
    justify-content: space-between;
    span{
      font-size:32px;
      line-height:38px;
      color:white;
    }
  }
}
</style>
