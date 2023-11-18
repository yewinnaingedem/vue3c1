<template>
    <div class="card" style="width : 18rem ">
        <div class="card-body">
            <div class="card-title">{{ user.name }}</div>
            <div class="card-title">{{ user.age }}</div>
            <div class="card-title">{{ user.address }}</div>
            <button class="btn btn-primary" @click="showUsers()">Show User</button>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'UserComponent' ,
        props : {
            user : Object ,
            showUsers : Function , 
        },

    }
</script>