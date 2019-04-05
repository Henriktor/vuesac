<template>
    <div class="hello">
        <h1>{{ revMsg }}</h1>
        <li><a href="https://cloud.diaspora.nu" target="_blank" rel="noopener">diaspora</a></li>
        </ul>
    </div>
</template>
<script>
export default {
    props: {
        msg: String
    },
    computed: {
        // a computed getter
        revMsg: function() {
            // `this` points to the vm instance
            return this.msg.split('').reverse().join('')
        }
    }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
    text-align: left;
}

p {
    color: #42b981;

}
</style>