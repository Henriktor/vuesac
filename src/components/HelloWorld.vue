<template>
    <div class="hello">
        <h1>{{ revMsg }}</h1>
        
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

h1 {
    margin: 2px 4px 21px;
    
    text-decoration: none;

}
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
    color: #20b54a;
    border-bottom: 10px
}

p {
    color: #42b981;

}



</style>