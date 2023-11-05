<template>
    <AddContent></AddContent>
    <AddHeader></AddHeader>
    <AddNav></AddNav>
</template>

<script>    
    import AddContent  from './AddContent.vue';
    import AddHeader from './AddHeader.vue';
    import AddNav from './AddNav.vue';

    export default {
        name : 'SimplePage' ,
        components : {
            AddContent , 
            AddHeader ,
            AddNav ,
        }
    }
</script>