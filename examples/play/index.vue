<template>
  <div style="margin: 20px;">
    <div>{{ value }}</div>
    <el-cascader
      v-model="value"
      placeholder="请选择所属组织"
      style="width: 300px;"
      :options="groupList"
      filterable
      clearable
      :props="{
        multiple: true,
        value: 'id',
        label: 'name',
        children: 'sub_list',
        checkStrictly: true,
        emitPath: false,
      }"
  />
  </div>
</template>

<script>
const mock = [
  {
    "id": 1,
    "name": "董菲菲测试",
    "pid": 0,
    "is_mch": 1,
    "is_virtual": 0,
    "is_on": 1,
    "sub_list": [
      {
        "id": 11,
        "name": "项目实施",
        "pid": 384,
        "is_mch": 0,
        "is_virtual": 0,
        "is_on": 1,
        "sub_list": [
          {
            "id": 111,
            "name": "一组",
            "pid": 564,
            "is_mch": 0,
            "is_virtual": 0,
            "is_on": 1
          },
          {
            "id": 112,
            "name": "二组",
            "pid": 564,
            "is_mch": 0,
            "is_virtual": 0,
            "is_on": 1,
            "sub_list": [
              {
                "id": 1121,
                "name": "测试测试改改",
                "pid": 566,
                "is_mch": 0,
                "is_virtual": 0,
                "is_on": 1
              }
            ]
          }
        ]
      },
      {
        "id": 12,
        "name": "后台测试",
        "pid": 384,
        "is_mch": 0,
        "is_virtual": 0,
        "is_on": 1,
        "sub_list": [
          {
            "id": 121,
            "name": "超长部门超长部门超长部门超长部门超长部门超长部门超长部门超长部门",
            "pid": 140,
            "is_mch": 0,
            "is_virtual": 0,
            "is_on": 1
          }
        ]
      }
    ]
  }
]
  export default {
    data() {
      return {
        value: [ 1, 11, 12 ],
        groupList: mock
      };
    }
  };
</script>
