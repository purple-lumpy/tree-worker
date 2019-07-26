<template>
    <div>
        <Tree @changeSelect="handleChangeSelect" :myData="treeData" />
    </div>
</template>

<script>
    import Tree from './tree/TreeInterface'
    import {data as mockData} from '../mock'

    export default {
        name: "TreeExample",
        components: {
            Tree
        },
        data: function () {
            return {
                treeData: mockData
            }
        },
        methods: {
            handleChangeSelect (val) {
                console.log('选择的路径为 ', val)
            }
        }
    }
</script>

<style scoped>

</style>
