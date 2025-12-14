<template>
  <div>
  <button @click="cs = !cs">click me {{ cs }}</button>
  <button @click="getSelected">get</button>
  <el-tree
    ref="tree"
    :data="data"
    show-checkbox
    node-key="id"
    side-control
    :check-strictly="cs"
    :default-expanded-keys="[2, 3]"
    :default-checked-keys="[1]"
    :props="defaultProps">
  </el-tree>
  </div>
</template>

<script>
  export default {
    methods: {
      getSelected() {
        console.log(this.$refs.tree)
      }
    },
    data() {
      return {
        cs: true,
        data: [{
          id: 1,
          label: '一级 1',
          children: [{
            id: 4,
            label: '二级 1-1',
            children: [{
              id: 9,
              label: '三级 1-1-1'
            }, {
              id: 10,
              label: '三级 1-1-2'
            }]
          }]
        }, {
          id: 2,
          label: '一级 2',
          children: [{
            id: 5,
            label: '二级 2-1'
          }, {
            id: 6,
            label: '二级 2-2'
          }]
        }, {
          id: 3,
          label: '一级 3',
          children: [{
            id: 7,
            label: '二级 3-1'
          }, {
            id: 8,
            label: '二级 3-2'
          }]
        }],
        defaultProps: {
          children: 'children',
          label: 'label'
        }
      };
    }
  };
</script>