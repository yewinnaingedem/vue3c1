<template >
    <div class="container">
        <SingleSlot>
            <h1>This parent signel slot</h1>
            <h2>I amn't feeling Good Today , today I haven't been somking for the whole day I kind of different to do it ;</h2>
            <p>I am feeling differently compare the ohter day today </p>
            <img src="../../../assets/logo.png" alt="">
        </SingleSlot>
        <hr>
        <MultiSlot>
            <template v-slot:header>
                <img src="../../../assets/logo.png">
            </template>
            <template v-slot:body>
                <ul class="list-group my-3">
                    <li class="list-group-item">Item 1</li>
                    <li class="list-group-item">Item 2</li>
                    <li class="list-group-item">Item 3</li>
                    <li class="list-group-item">Item 4</li>
                    <li class="list-group-item">Item 5</li>
                </ul>
            </template>
            <template v-slot:footer>
                <button class="btn btn-primary">Footer Slot</button>
            </template>
        </MultiSlot>
    </div>
</template>

<script>
    import MultiSlot from "./MultiSlot.vue" ;
    import SingleSlot from './Single-Slot.vue';
    export default {
        name : "SlotPlayGround" ,
        components : {
            SingleSlot ,
            MultiSlot
        }
    }
</script>