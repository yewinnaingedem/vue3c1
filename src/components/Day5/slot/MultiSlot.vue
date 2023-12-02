<template>
    <h1>Multi Slot/</h1>
    <slot name="header">
        <p>this is Header</p>
    </slot>
    <slot name="body">
        <p>this is Body</p>
    </slot>
    <slot name="footer">
        <p>this is Footer </p>
    </slot>
</template>

<script>
    export default {
        name : "MultiSlot" ,
    }
</script>