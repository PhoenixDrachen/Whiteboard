<template>
    <div class="developerClientCard">
        <h2>{{ this.developerName }}</h2>
    </div>
</template>

<script>
export default {
  props: {
    developer: Object
  },
  data () {
    return {
      developerName: this.developer.name
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/variables.scss';
    .developerClientCard{
        width:100%;
        height:550px;
        background-color: $dark_accent;
        border-radius:25px;
        box-shadow: 10px 10px 20px rgba(0,0,0,.5);
        padding-left:5px;
        padding-right:5px;
        h2{
            text-align: center;
            padding-top:15px;
            font-size:45px;
            color:$light_base;
            font-family: 'Cuprum';
            font-weight:700;
            border-bottom: 8px solid $light_base;
        }
    }
</style>
