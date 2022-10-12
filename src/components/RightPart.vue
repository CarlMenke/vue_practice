<template>
    <div>
        <h2>{{typeof parseInt(number)}}</h2>
    </div>
</template>

<script>
    export default {
        name: 'RightPart',
        props:{
            number:String
        }
    }
</script>

<style>
    h2{
        background-color:aqua;
    }
</style>