<script>
export default {
    props: {
        helloMsg: String,
    },
    render: function(createElement) {

        return createElement('h3', this.helloMsg)
    }

}
</script>
<style scoped>

h3 {
    margin: 40px 0 0;
    padding: 10px;
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



