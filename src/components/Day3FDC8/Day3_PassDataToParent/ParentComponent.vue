<template>
    <div class="container">
        <h1>Child Component</h1>
        <div>{{ name }}</div>
        <ChildComponent :updateName="updateName"></ChildComponent>
    </div>

</template>
<script>
    import ChildComponent from "./ChildComponent.vue";
    export default {
        name : "ParentComponent" ,
        components : {ChildComponent} ,
        data () {
            return {
                name : "Empty Name" ,
            }
        },
        methods : {
            updateName (name ) {
                this.name = name ;
            }
        }
    }
</script>