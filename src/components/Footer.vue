<template>
  <footer>
      Studies <span>{{ footer.framework }}</span> By {{ footer.author }}
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        footer: Object, // String, Number, Object, Array,
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
