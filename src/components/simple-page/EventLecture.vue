<template>
    <h1>Event Lecture </h1>
    <div class="container pt-3">
        <button class="btn btn-primary mb-3" v-on:click="showMessage('I am primary button')">Primary Button </button>
        <br>
        <button class="btn btn-info" v-on:click="showMessage('I am info button')"   >Info Button</button>
    </div>

    <div class="card mt-3" style="width: 150px;">
        <div class="card-body text-center bg-dark rounded">
            <div class="text-warning h5">
                {{ count }}
            </div>
            <button v-on:click="increase()" class="btn btn-primary me-1">+</button>
            <button v-on:click="decrease()" class="btn btn-danger">-</button>
        </div>

    </div>
    
</template>

<script>
    export default {
        name : 'EventLecture' ,
        methods : {
            showMessage (event) {
                alert(event);
            },
            increase () {
                this.count ++ ;
            },
            decrease () {
                this.count -- ;
            }
        },
        data() {
            return {
                count : 0 ,
            }
        }
    }
</script>