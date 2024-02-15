<template>
    <div>
        <h2>This is a Popup</h2>
        <button @click="$emit('close', 'Iyanuloluwa')"> Close Popup</button>
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        emits: ['close']
        
    }
</script>

<style scoped>

</style>