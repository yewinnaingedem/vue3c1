<template>
    <div class="container">
        <h1>Form And Validation</h1>
        <div class="row">
            <div class="col-md-6">
                <pre>
                    {{ form }}
                </pre>
            </div>
            <div class="col-md-6">
                <pre>
                    {{ Object || form }}
                </pre>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-6">
                <div class="mb-3">
                    <label class="form-label">Name</label>
                    <input type="text" class="form-control" v-model="form.name" placeholder="Enter Name">
                </div>
                <div class="mb-3">
                    <label class="form-label">Age</label>
                    <input type="number" class="form-control" v-model="form.age" placeholder="Enter Age">
                </div>
                <div class="mb-3">
                    <div class="form-check">
                        <input class="form-check-input" type="radio" value="male" v-model="form.gender" id="male">
                        <label class="form-check-label" for="male">
                            Male
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" value="female" v-model="form.gender" id="female">
                        <label class="form-check-label" for="female">
                            Female
                        </label>
                    </div>
                </div>
                <div class="mb-3">
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="stundent" v-model="form.profession"
                            id="stundent">
                        <label class="form-check-label" for="stundent">
                            Stundent
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="teacher" v-model="form.profession"
                            id="teacher">
                        <label class="form-check-label" for="teacher">
                            Teacher
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="developer" v-model="form.profession"
                            id="developer">
                        <label class="form-check-label" for="developer">
                            Developer
                        </label>
                    </div>
                </div>
                <div class="mb-3">
                    <button class="btn btn-primary" @click="sumbit">Sumbit</button>
                </div>
                <hr>
                <p v-if="form.error.length == 0">Form Is Validate</p>
                <p v-else>Form is Invalidate</p>
            </div>
            <div class="col-6">
                <p class="text-danger" v-for="(error, index) in form.error" :key="index">
                    {{ error }}
                </p>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "FromAndValidation",
    data() {
        return {
            form: {
                name: null,
                age: null,
                gender: null,
                profession: [],
                error: [],
            }
        }
    },
    methods: {
        // sumbit() {
        //     for (const key in this.form) {
        //         console.log("Key is :" + key );
        //         console.log("Value is :" + this.form[key]);
        //         console.log('-----------------');
        //     }
        // }
        sumbit() {
            this.validation();
            Object.keys(this.form).forEach(value => {
                console.log(value, this.form[value]);
                console.log('-------------');
            });
        },
        validation() {
            this.form['error'] = [];
            if (this.form['name'] == null) {
                this.form['error'].push('name');
            }
            if (this.form['age'] == null) {
                this.form['error'].push('age');
            }
            if (this.form['gender'] == null) {
                this.form['error'].push('gener');
            }
            if (this.form['profession'].length == 0) {
                this.form['error'].push('profession');
            }
        }
    }
}
</script>