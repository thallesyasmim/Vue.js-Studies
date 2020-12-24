<template>
  <section>
      <div></div>
      <div></div>
  </section>
</template>

<script>
export default {
    name: 'QuadToCircle'
}
</script>

<style scoped> 
    div {
        width: 200px;
        height: 200px;
        margin-top: 5px;
        background-color: #2c3e50;
        box-shadow: 7px 5px 15px rgba(0, 0, 0, 0.20);
        border-radius: 5px;
        animation: Transform 3s infinite;
        animation-timing-function: ease-in-out;
    }

    @keyframes Transform {
        to {
            border-radius: 5px;
        }

        100% {
            border-radius: 50%;
        }
    }

</style>