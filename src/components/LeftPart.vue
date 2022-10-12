<template>
    <div>
        <div>image src {{image}}</div>
    </div>
</template>

<script>
    export default {
        name:'LeftPart',
        props: ['image']
    }
</script>

<style>
    img{
        width:10%;
    }
</style>