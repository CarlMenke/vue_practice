<template>
    <div>
        <h3>{{msg}}</h3>
    </div>
</template>

<script> //must always export an object
    export default {
        name: 'GoodComponent',
        props:{
            msg: String,
        }
    }
</script>
 
<style>
    h3 {
        color: #80cbc4;
    }
</style>
