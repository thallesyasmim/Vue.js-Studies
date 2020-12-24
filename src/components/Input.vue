<template>
  <input type="text" :value="name">
</template>

<script>
export default {
    name: 'Input',
    data() {
        return {
            name: 'Thalles Gabriel'
        }
    }
}
</script>

<style scoped>
    input {
        border: 2px solid #2c3e50;
        border-radius: 5px;
        margin: 7px 0 20px;
        padding: 10px 10px; 
        font-weight: 600;
        color: #18222c;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.25);
    }
</style>