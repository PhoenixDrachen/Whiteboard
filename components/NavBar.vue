<template>
    <div>
        <div class="navbar_wrapper">
            <a href="#">test</a>
            <a href="#">test</a>
            <a href="#">test</a>
            <a href="#">test</a>
            <a href="#">test</a>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.navbar_wrapper{
    position:absolute;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    left:calc(50% - 225px);
    top:15px;
    height:150px;
    width:450px
}
</style>
