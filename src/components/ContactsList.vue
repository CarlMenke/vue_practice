<template>
    <div>
        <div :key="phoneNumber.id" v-for="phoneNumber in phoneNumbers">
            <h4 v-if="phoneNumber.phoneNumber.includes('(')">{{phoneNumber.phoneNumber}}</h4>
            <h4 v-else>Not Valid</h4>
        </div>
    </div>
</template>

<script> //must always export an object
    export default {
        name: 'ContactsList',
        props:{
            phoneNumbers: Array,
        }
    }
</script>
 
<style>
    h3 {
        color: #80cbc4;
    }
</style>