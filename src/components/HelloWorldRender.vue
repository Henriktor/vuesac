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




