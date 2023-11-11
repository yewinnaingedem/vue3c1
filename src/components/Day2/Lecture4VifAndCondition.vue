<template>
    <div class="container pt-3">
        <h4>Vue ( v-if , v-else and v-for )</h4>
        <button class="btn btn-primary" v-on:click="toggle()">
            {{ show ? 'Hide' : 'Show' }}
        </button>
        <br>
        <img v-if="show" src="../../assets/logo.png" alt="Logo" width="100px" height="100px" class="rounded overflow-hidden">
        <p v-else > Image is hiding</p>
        <hr>
        <ul class="list-group">
            <li class="list-group-item" v-for="technology in technologies " :key="technology" >{{ technology }}</li>
        </ul>
        <hr>
        <table class="table table-dark text-center">
            <thead>
                <tr>
                    <th scope="col">Name</th>
                    <th scope="col">Age</th>
                    <th scope="col">Address</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="user in users" :key="user">
                    <td>{{ user.name }}</td>
                    <td>{{ user.age }}</td>
                    <td>{{ user.address }}</td>
                </tr>
             </tbody>
        </table>
    </div>
</template>
<script>
    export default {
        name : "Lecture4VifAndConditon" ,
        data () {
            return {
                show : false ,
                technologies : [
                    'PHP' ,
                    "JAVA" ,
                    "C#" ,
                    'C++' ,
                    'PYThON' ,
                    'CSS' ,
                    'HTML' ,
                    'Native'
                ],
                users : [
                    {
                        name : "Aung Aung ",
                        age  : 17 ,
                        address : "Mandalay"
                    },
                    {
                        name : 'Su Su',
                        age : 25 ,
                        address : "Yangon"
                    },
                    {
                        name : "Kaung Hlaing" ,
                        age : 21 ,
                        address : "Saking "
                    }
                ]
            }
        },
        methods : {
            toggle () {
                this.show = !this.show ;
            }
        }
    }
</script>