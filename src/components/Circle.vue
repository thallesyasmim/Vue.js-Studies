<template>
    <article>
        <section v-for="(circle, index) in circles" :key="circle.id">
            <div>{{ index }}</div>
            <div id="circle">{{ circle.fruit }}</div>
        </section>
        <h1>Register: {{ inputField }}</h1>
        <input type="text" placeholder="Add Circles" v-model="inputField">
        <button @click="addCircle(inputField)">Add</button>
    </article>
</template>

<script>
export default {
    name: 'QuadToCircle',
    data() {
        return {
            circles: [
                { id: 1, fruit: "Banana" }, 
                { id: 2, fruit: "Orange" }, 
            ],
            inputField: ''
        }
    },
    methods: {
        addCircle(fruit) {
            const { id } = this.circles[this.circles.length - 1]
            const fruits = ["Apple", "Mango"]
            if(fruit !== '') {
                fruits.push(fruit)
            }
            const data = {
                id: id + 1,
                fruit: fruits[Math.floor(Math.random() * fruits.length)]
            }
            this.circles.push(data)
        }
    }
}
</script>

<style scoped> 
    div {
        width: 115px;
        height: 115px;
        margin-top: 30px;
        background-color: #2c3e50;
        box-shadow: 10px 8px 15px rgba(0, 0, 0, 0.25);
        border-radius: 5px;
        animation: Transform 1.5s infinite alternate;
        animation-timing-function: ease-in-out;
    }

    div#circle {
        background-color: #18222c;
        margin-bottom: 15px;
    }

    @keyframes Transform {
        to {
            border-radius: 5px;
            transform: rotate(0deg);
        }

        100% {
            border-radius: 50%;
            transform: rotate(90deg);
        }
    }

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

    button {
        padding: 10px;
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