<template>
    <div class="container">
        <h1>Watch</h1>
        <div class="mb-3">
            <h3 class="text-center" style="width:75px">{{ count }}</h3>
            <button class="btn btn-primary me-2" @click="increase()">+</button>
            <button class="btn btn-danger" @click="decrease()">-</button>
        </div>
    </div>
</template>

<script>
    export default {
        name : "WatchComponent" ,
        data () {
            return {
                count : 0 ,
            }
        },
        methods : {
            increase () {
                this.count++ ;
            },
            decrease () {
                this.count -- ;
            }
        },
        watch : {
            count (val) {
                if(val > 5){
                    this.count = 0 
                    alert('Stop Counting');
                }
            }
        }
    }

</script>