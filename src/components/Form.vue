<template>
  <form>
     <h1>Register</h1>
     <input type="text" placeholder="Add Circle">
  </form>
</template>

<script>
    export default {
        name: 'Form'
    }
</script>

<style scoped>
    h1 {
        color: #2c3e50;
        margin: 20% 0 10px;
    }

    input {
        border: 2px solid #2c3e50;
        border-radius: 5px;
        margin: 7px 5px 20px;
        padding: 10px 10px; 
        font-weight: 600;
        color: #18222c;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.25);
    }
</style>