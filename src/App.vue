<template>
    <div id="app">
        <main class="content">
                <ul class="menu">
                   <li class="wrap"><img alt="Vue logo" src="./assets/logo.png" align="left"></li>
                </ul>
            <ul class="wrap-menu">
                <form v-on:submit.prevent="onSubmit">
                    <input class="button" type="text" ref="inputField" placeholder="Skriv här">
                    <button class="button" type="submit" value="Submit">Submit</button>
                    <button class="button" type="submit" value="Submit">Reverse</button>
                </form>
            </ul>
        </main>
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