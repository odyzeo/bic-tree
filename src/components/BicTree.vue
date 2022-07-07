<template>
    <div class="bic-tree">
        <h1 v-text="c.title"></h1>
        {{ b }}
        <hr>
        {{ c }}
        <hr>
        {{ aggregations }}
    </div>
</template>

<script>
export default {
    name: 'BicTree',
    props: {
        aggregations: {
            type: Object,
            default: null,
        },
        b: {
            type: String,
            default: null,
        },
        c: {
            type: Number,
            default: null,
        },
    },
};
</script>

<style lang="less">
.bic-tree {

}
</style>
