<template>
    <div class="store">
        <span class="">

                        <h2 class="icon-magnifying_glass"></h2>
            
                    </span>
    </div>
</template>
<script>
export default {
    props: {
        msg: String
    },
    render: function(createElement) {

        return createElement('p', this.msg)
    }
}
</script>