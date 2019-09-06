<template>
  <div class="launchCard">
    <h2>To Be Launched</h2>
    <div class="bottomBar" />
    <div class="launchHeader">
      <p class="dueDateHeader">
        Date
      </p>
      <p class="clientHeader">
        Client
      </p>
      <p class="assignedHeader">
        Assigned
      </p>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/variables.scss';
    .launchCard{
        width:100%;
        height:550px;
        background-color: $dark_accent;
        border-radius:10px;
        box-shadow: 10px 10px 20px rgba(0,0,0,.5);
        padding-left:10px;
        padding-right:10px;
        h2{
            text-align: center;
            padding-top:15px;
            font-size:45px;
            color:$light_base;
            font-family: $header_font;
            font-weight:700;
        }
        .bottomBar{
          height:8px;
          background-color:$light_base;
          border-radius:25px;
        }
        .launchHeader{
          margin-top:5px;
          display:flex;
          flex-direction:row;
          p{
            width:50px;
            flex-grow:1;
            text-align:center;
            font-size:24px;
            font-weight:700;
            color:$light_base;
            font-family:$body_font;
            border-bottom:2px solid $light_base;
            margin-left:5px;
            margin-right:5px;
            justify-content: space-between;
            &:after{
              content:' ';
              height:2px;
              border-radius:25px;
              background-color:$light_base;
              width:50px;
            }
          }
          .clientHeader{
            flex-grow: 5
          }
          // .dueDateHeader{
          //   text-align: left;
          // }
          // .assignedHeader{
          //   text-align:right;
          // }
        }
    }
</style>
