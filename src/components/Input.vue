<template>
    <div>
       <input type="text" v-model="twoWay">
       <input type="text" :value="name">
       <input type="text" v-model="twoWay">
    </div>
</template>

<script>
export default {
    name: 'Input',
    data() {
        return {
            name: 'One Way Data Binding',
            twoWay: 'Two Way Data Binding'
        }
    }
}
</script>

<style scoped>
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