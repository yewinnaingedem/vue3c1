<template>
    <div class="container">
        <div class="mb-3">
            <label class="form-label">Dollar</label>


            <input type="number" class="form-control" v-model="dollar" placeholder="Enger Dollar">
        </div>
        <div class="mb-3">
            <label class="form-label">MMK</label>
            <input type="number" class="form-control"  readOnly :value="getValue()" placeholder="Enger MMK">
        </div>
        <div class="mb-3">
            <label class="form-label">Dollar</label>
            <input type="number" class="form-control"  :value="getData" placeholder="Enger Dollar">
        </div>
    </div>
</template>

<script>
    export default {
        name: "ComputedValue",
        data() {
            return {
                dollar: null,
                rates: 3500,
                mmk: 0,
            }
        },
        methods : {
            getValue () {
                return this.dollar * this.rates ;
            }
        },
        computed : {
            getData () {
                return this.dollar * this.rates ;
            }
        }
    }
</script>