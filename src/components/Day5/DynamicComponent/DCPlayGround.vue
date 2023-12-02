<template>
    <div class="container mt-3" >
        <ul class="nav mb-3">
            <li class="nav-item">
                <button class="nav-link" @click="showTab('Component1')">Java</button>
            </li>
            <li class="nav-item">
                <button class="nav-link " @click="showTab('Component2')">PHP</button>
            </li>
            <li class="nav-item">
                <button class="nav-link " @click="showTab('Component3')">Python</button>
            </li>
        </ul>
        <component :is="tab"></component>
    </div>
</template>

<script>
    import Component1 from "./Component1.vue";
    import Component2 from "./Component2.vue";
    import Component3 from "./Component3.vue";

    export default {
        name : "DCPlayGround" ,
        data () {
            return {
                tab : "Component1" ,
            }
        },
        methods : {
            showTab (tab ) {
                this.tab = tab ;
                console.log(this.tab);
            }
        },
        components : {
            Component1 , 
            Component2 ,
            Component3 
        }
    }
</script>