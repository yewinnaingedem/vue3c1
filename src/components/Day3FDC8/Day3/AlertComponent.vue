<template>
    <div  :class="['alert', 'alert-'+type , 'alert-dismissible' , 'fade' , 'show']" role="alert">
        <strong>{{ title }}</strong> {{ text }}
        <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
    </div>
</template>
<script>
// :class="getClass()"

export default {
    name : "AlertComponent" ,
    props : {
        type : {
            type : String ,
            default : 'danger'
        } ,
        title : {
            type : String ,
            default : "Danger Alert !",

        } ,
        text : {
            type : String ,
            default : 'This is danger Alert' ,
            required : true ,
        } ,
    },
    methods : {
        getClass () {
            return `alert alert-${this.type} alert-dismissible fade show` ;
        }
        
    }
}
</script>