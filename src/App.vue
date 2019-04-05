<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <a href="https://cloud.diaspora.nu" target="_blank" rel="noopener"><HelloWorld msg="diasporA" /></a>
        <form v-on:submit.prevent="onSubmit" >
        <input type="text" ref="inputField" placeholder="Skriv här">
        <button type="submit" value="Submit">Submit</button>
        </form>
        <HelloWorldRender v-bind:helloMsg="hello" />

    </div>
</template>
<script>
import test from './components/HelloWorld.vue'

import HelloWorldRender from './components/HelloWorldRender.vue'


export default {
    name: 'app',
    data: function() {
        return {
            hello: null
        }
    },
    methods: {
        onSubmit() {
            // eslint-disable-next-line
            this.hello = this.$refs.inputField.value
          },
        },
    components: {
        'HelloWorld': test,
        'HelloWorldRender': HelloWorldRender,
    }
}
</script>
<style>
#app {
    
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 10px;
}
</style>