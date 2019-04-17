<script>
export default {
    props: {
        helloMsg: String,
    },
    render: function(createElement) {

        return createElement('p', this.helloMsg)
    }

}
 </script>