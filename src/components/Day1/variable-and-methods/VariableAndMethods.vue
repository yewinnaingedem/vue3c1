<template>
    <h1>Variable And Methods</h1>

    <h2> With Variable </h2>
    <p>Name - {{ name }}</p>
    <p>Email - {{ email }}</p>
    <p>Age - {{ age }}</p>

    <h2>With Methods</h2>
    <p>Name {{ getName() }}</p>
    <p>Eamil {{ getEmail() }}</p>
    <p>Age {{ getAge() }}</p>

    <h2>With Data</h2>
    <p>Name = {{ getData().name }}</p>
    <p>Email = {{ getData().email }}</p>
    <p>Age = {{ getData().age }}</p>
</template>

<script>
    export default {
        name : 'VariableAndMethods',
        data() {
            return {
                name : "Mg Mg" ,
                email : 'mgmg@sf.com',
                age : 17 
            }
        },
        methods : {
            getName () {
                return this.name ;
            },
            getEmail () {
                return this.email ;
            },
            getAge () {
                return this.age ;
            },
            getData () {
                return {
                    name : "Mg Mg" ,
                    email : 'mgmg@sf.com',
                    age : 17 
                }
            }
        }
    }
</script>