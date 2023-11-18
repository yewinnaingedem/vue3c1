<template>
    <div class="container">
            <div class="container" v-html="element1 + element2 + element3 ">

            </div>
            <hr>
            <h1 :class="getClass()" class="rounded">Class Binding</h1>
    </div>
</template>

<script>
    export default {
        name : "HTMLAndClassBinding" ,
        data () {
            return {
                element1 : "<h1>HTML Binding</h1>",
                element2 : "<h1>Header 2</h1>",
                element3 : "<h1>Header 3</h1>",
            }
        },
        methods : {
            getClass () {
                return {
                    bgColor : true ,
                    textWhite : true ,
                    textAlign : true ,
                }
            }
        }
    }
</script>

<style scope>
    .bgColor {
        background : tomato ;
    }
    .textAlign {
        text-align :center ;
    }
    .textWhite {
        color :white ;
    }
</style>