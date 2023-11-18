<template>
    <h1>Child Component</h1>
    <button class="btn btn-primary" v-on:click="updateName('Kyaw Kyaw')">Updata Name</button>
</template>
<script>
    export default {
        name : "ChildComponent" ,
        props : {
            updateName : Function ,
        }
    }
</script>