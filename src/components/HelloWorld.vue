<template>
    <div  class="hello">
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
