<template>
    <div class="wrapper">
        <Typehead></Typehead>
        <USMap></USMap>
    </div>
</template>

<script>
import { onMounted, ref } from 'vue' 
import Typehead from './components/Typehead'
import USMap from './components/GoogleMap.vue'



export default {
    name: 'App',
    components: {
        Typehead,
        USMap,
    },
}
</script>

<style>

    *  {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    html {
        font-size: min(calc(11px + 0.4vw), 16px);
    }
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        width: 100%;
        height: 100vh;
        display: grid;
    }
    .wrapper {
        margin: auto;
        width: min(60em, 90%);
        /* border: 1px solid black; */
        padding: 2em 1em;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    input {
        font: inherit;
        padding: 0.8em 1em;
        width: min(40em, 100%);
        margin-bottom: 1em; 
    }
    .google-map {
        width: 100%;
        height: 60vh;
    }

</style>
