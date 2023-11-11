<template>
    <div class="container">
        <h2>Two Way Data Binding </h2>
        <hr>
        <h1>Variable Binding</h1>
        <div class="mb-3">
            <label for="" class="form-label">{{ name }}</label>
            <input type="text" class="form-control" v-model="name">
        </div>
        <div class="mb-3">
            <button class="btn btn-primary" v-on="changeName()">Change Name</button>
        </div>
        <hr>
        <h1>Object Binding </h1>
        <div class="mb-3">
            <label for="" class="form-label">{{ user.name }}</label>
            <input type="text" class="form-control" v-model="name">
        </div>
        <div class="mb-3">
            <label for="" class="form-label">{{ user.age }}</label>
            <input type="text" class="form-control" v-model="name">
        </div>
        <div class="mb-3">
            <label for="" class="form-label">{{ user.address }}</label>
            <input type="text" class="form-control" v-model="name">
        </div>
        <div class="mb-3">
            <pre>{{ getUser() }}</pre>
        </div>
        <hr>
        <h1>Check box Binding In Vue</h1>
        <div class="mb-3">
            <input type="checkbox" class="form-check-input" value="PHP" id="PHP" v-model="technologies">
            <label class="form-check-label" for="PHP">PHP</label>
        </div>
        <div class="mb-3">
            <input type="checkbox" class="form-check-input" value="Node.js" id="Node.js" v-model="technologies">
            <label class="form-check-label" for="Node.js">PHP</label>
        </div>
        <div class="mb-3">
            <input type="checkbox" class="form-check-input"  value="html" id="html" v-model="technologies">
            <label class="form-check-label" for="html">PHP</label>
        </div>
        <div>
            <pre>
                {{ technologies }}
            </pre>
        </div>
        <hr>
        <h1>Two Way Binding Radio</h1>
        <div class="mb-3">
            <input type="radio" class="form-radio-input mr-3" id="student" value="Student" v-model="profession" >
            <label for="student">Student</label>
        </div>
        <div class="mb-3">
            <input type="radio" class="form-radio-input mr-3" id="developer" value="Developer" v-model="profession" >
            <label for="developer">Developer</label>
        </div>
        <div class="mb-3">
            <input type="radio" class="form-radio-input mr-3" id="teacher"  value="Teacher" v-model="profession" >
            <label for="teacher">Teacher</label>
        </div>
        <hr>
        <div>
            {{ profession }}
        </div>
    </div>

</template>
<script>
    
     export  default{
        name : "TwoWayBinding" ,
        data () {
            return {
                name : "Kyaw Kyaw"  ,
                user : {
                    name : null ,
                    age : null , 
                    address : null ,
                },
                technologies : [] ,
                profession : 'Student' ,
            }
        },
        methods : {
            changeName () {
                this.name = "Ye Win Naing" ;
            },
            getUser () {
                return this.user ;
            }
        }
    }
</script>
<style>
    .mr-3 {
        margin-right : 5px ;
    }
</style>