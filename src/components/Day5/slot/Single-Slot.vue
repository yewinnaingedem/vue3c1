<template>
    <div class="container">
        <h1>Single Slot</h1>
        <slot>
            <h1>This is Element</h1>
        </slot>
    </div>

</template>
<script>
    export default {
        name : "singleSlot" ,
        
    }
</script>