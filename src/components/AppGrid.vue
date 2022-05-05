<template>
    <div>
        Content goes here 
    </div>
</template>

<script>
export default {
    name: 'AppGrid'
}
</script>

<style lang="scss">
@import '../style/variables';
@import '../style/general';
main{
    @include my-flex;
    height: 80px;
    background-color: #1c1c1c;
    color: $colortextmain;
}
</style>