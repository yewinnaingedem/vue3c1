<template>
    <div class="container">
        <h1>Pass Data to Child</h1>
        <AlertComponent type="warning" title="Alert Waring " text="This is alert warning"></AlertComponent>
        <AlertComponent type="info" title="Info Warning" text="This is info warning"></AlertComponent>
        <AlertComponent type="primary" title="Primary Waring " text="This is primary waring"></AlertComponent>
        <hr>
        <h1>Alert Default</h1>
        <AlertComponent></AlertComponent>
        <hr>
        <h1>Object Component</h1>
        <UserComponent :user="user" :showUsers="showUser"></UserComponent>
        <hr>

        <h1>Table Component</h1>
        <TableComponent :table="data" ></TableComponent>
    </div>
</template>
<script>
    import AlertComponent from './AlertComponent.vue';
    import UserComponent from "./UserComponent.vue";
    import TableComponent from "./TableComponent.vue" ;
    export default {
        name : "ParentComponent" ,
        components : {
            AlertComponent ,
            UserComponent ,
            TableComponent ,
        },
        data () {
            return {
                user : {
                    name : "Mg Mg" ,
                    age : 21 ,
                    address : "Hlandan"
                },
                data : {
                    columns : ['First' , 'Last' , 'Age'] ,
                    rows : [
                        {
                            first : "Mg" ,
                            Last : "Ye" ,
                            age : 21 ,
                        },
                        {
                            first : "Mg" ,
                            Last : "Phone" ,
                            age : 3 ,
                        },
                        {
                            first : "Mg" ,
                            Last : "Thu" ,
                            age : 18 ,
                        }
                    ]
                }
            }
        },
        methods : {
            showUser () {
                console.log(this.user);
            }
        }
    }
</script>