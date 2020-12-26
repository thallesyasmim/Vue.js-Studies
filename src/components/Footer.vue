<template>
  <footer>
      Studies <span>{{ framework }}</span> By {{ author }}
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        framework: String, // Number, Object, Array,
        author: String
    }
}
</script>

<style scoped>
    footer {
        padding: 50px 0;
        font-family: monospace;
        font-size: 20px;
        font-weight: 700;
        color: #2c3e50;
    }

    footer span {
        color: #18222c;
    }
</style>>
