<template>
    <div class="app">
        <aside class="app__aside">
            <a
                v-for="tree in $options.TREES"
                :key="tree.title"
                href
                class="app__link"
                @click.prevent="selectTree(tree)"
                @keydown="selectTree(tree)"
                v-text="tree.title"
            ></a>
        </aside>

        <main class="app__main">
            <bic-tree
                :aggregations="localTree.aggregations"
                :b="localTree.bic"
                :c="localTree.category"
            ></bic-tree>
        </main>
    </div>
</template>

<script>
import BicTree from '@/components/BicTree';
import TREE_A from '@/data/bic/ag-c-1.json';
import TREE_B from '@/data/bic/ag-c-1-b-AFJ.json';
import TREE_C from '@/data/bic/ag-c-24-b-KF.json';

export default {
    TREES: [{
        title: 'Tree A',
        tree: TREE_A,
    }, {
        title: 'Tree B',
        tree: TREE_B,
    }, {
        title: 'Tree C',
        tree: TREE_C,
    }],
    name: 'App',
    components: { BicTree },
    data() {
        return {
            localTree: null,
        };
    },
    created() {
        this.selectTree(this.$options.TREES[0]);
    },
    methods: {
        selectTree(tree) {
            this.localTree = tree.tree;
        },
    },
};
</script>

<style lang="less">
.app {
    display: flex;
    width: 1040px;
    margin: 0 auto;
}

.app__aside {
    flex: 0 0 auto;
    width: 200px;
}

.app__main {
    flex: 1 1 auto;
}

.app__link {
    display: block;
}
</style>
