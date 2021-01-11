<template>
    <article>
        <section v-for="circle in circles" :key="circle.id">
            <div></div>
            <div id="circle"></div>
        </section>
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
            ]
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

</style>