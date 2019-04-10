<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <form v-on:submit.prevent="onSubmit">
            <ul class="form">
                <li class="fourth first fullMobile">
                <input type="text" ref="inputField" placeholder="Skriv här"></textarea></li>
                <br>
                <button type="submit" value="Submit">Submit</button>
                <button type="submit" value="Submit">Reverse</button>
            </ul>
        </form>
        <HelloWorldRender v-bind:helloMsg="hello" />
        <HelloWorld v-bind:msg="msg" />
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