<template>
    <main>
        <div></div>
        <div id="quad"></div>
    </main>
</template>

<script>
    export default {
        name: 'Animation'
    }
</script>

<style scoped>
    div {
        width: 115px;
        height: 115px;
        margin-top: 5px;
        background-color: #2c3e50;
        border-radius: 5px;
        box-shadow: 7px 5px 15px rgba(0, 0, 0, 0.20);
        animation: move 3s infinite alternate;
        animation-timing-function: ease-in-out;
    }

    div#quad {
        animation-name: sideMove;
        background-color: #18222c;
    }

    @keyframes move {
        from {
            transform: translateX(100px);
        }
    }

    @keyframes sideMove {
        from {
            transform: translateX(-100px);
        }
}


</style>