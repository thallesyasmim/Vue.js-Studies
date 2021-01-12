<template>
    <div>
        <footer v-if="footer && !directive"> <!-- Directive: Attribute that does not exist in HTML -->
            Studies <span>{{ footer.framework }}</span> By {{ footer.author }}
        </footer>
        <footer id="one" v-else-if="!footer && directive">
            {{ directive }} 
        </footer>
         <footer v-else>
             directive: <span>v-else</span> 
        </footer>
        <footer v-show="!footer && !directive">
            <span>v-show</span> keeps the element on a page with "display: none;" 
        </footer>
        <footer v-show="!footer && !directive" :class="{'conditional-class': conditionalClass, '': !conditionalClass }">
            Using Conditional Class
        </footer>
        <button @click="changeClass" v-show="!footer && !directive">Change Class!</button>
    </div>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            conditionalClass: true
        }
    },
    props: {
        footer: Object, // String, Number, Object, Array,
        directive: String
    },
    methods: {
        changeClass: () => {
            alert('Funcionou!')
        }
    }
}
</script>

<style scoped>
    footer {
        padding: 20px 0;
        font-family: monospace;
        font-size: 20px;
        font-weight: 700;
        color: #2c3e50;
    }

    footer span {
        color: #18222c;
    }

    #one {
        margin-top: 40px;
    }

    .conditional-class {
        color: #18222c;
        background-color: #2c3e50;
    }

    button {
        padding: 20px;
        background-color: #2c3e50;
        border: none;   
        border-radius: 4px;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.25);
        color: #FFF;
        font-weight: 700;
        cursor: pointer;
        margin-top: 10px;
        transition: all 300ms;
    }

    button:hover {
        background-color: #FFF;
        color: #2c3e50;
    }

</style>
