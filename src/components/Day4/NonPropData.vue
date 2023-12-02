<template>
    <h3 v-bind="$attrs" ref="kk">Kyaw Kyaw</h3>
    <h3>Mg Mg</h3>
    <h2>{{item}}</h2>
    <button class="btn btn-primary" @click="getNonPropData()">Get Non Props Data</button>
</template>
    
<script>
    export default {
        name : "NonPropData" ,
        props : {
            item : String ,
        },
        methods : {
            getNonPropData () {
                console.log(this.$refs.kk);
                console.log(this.$refs.kk.getAttribute('name'));
            }
        }
    }
</script>