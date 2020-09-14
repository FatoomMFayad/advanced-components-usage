<template>
    <div>
        <h3>New Quote</h3>
        <button @click="counter = counter + 1">Increment Counter</button>
        <p>Counter: {{ counter }}</p>
    </div>
</template>
<script>
export default {
    data: function(){
        return {
          counter: 0  
        }
    },
    destroyed() {
        console.log('Destroyed')
    }
}
</script>>
<style scoped>
</style>