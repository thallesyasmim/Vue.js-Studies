<template>
    <div>
        <footer v-if="footer && !directive"> <!-- Directive: Attribute that does not exist in HTML -->
            Studies <span>{{ footer.framework }}</span> By {{ footer.author }}
        </footer>
        <footer v-else-if="!footer && directive">
            {{ directive }} 
        </footer>
        <footer v-show="!footer && !directive">
            <span>v-show</span> keeps the element on a page with "display: none;" 
        </footer>
    </div>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        footer: Object, // String, Number, Object, Array,
        directive: String
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
