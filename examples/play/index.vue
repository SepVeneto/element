<template>
  <div style="margin: 20px;">
    <el-cascader
      v-model="value"
      placeholder="请选择所属组织"
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
  export default {
    data() {
      return {
        value: [],
        groupList: 
[
  {
    "id": 384,
    "name": "董菲菲测试",
    "pid": 0,
    "is_mch": 1,
    "is_virtual": 0,
    "is_on": 1,
    "sub_list": [
      {
        "id": 564,
        "name": "项目实施",
        "pid": 384,
        "is_mch": 0,
        "is_virtual": 0,
        "is_on": 1,
        "sub_list": [
          {
            "id": 565,
            "name": "一组",
            "pid": 564,
            "is_mch": 0,
            "is_virtual": 0,
            "is_on": 1
          },
          {
            "id": 566,
            "name": "二组",
            "pid": 564,
            "is_mch": 0,
            "is_virtual": 0,
            "is_on": 1,
            "sub_list": [
              {
                "id": 570,
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
        "id": 140,
        "name": "后台测试",
        "pid": 384,
        "is_mch": 0,
        "is_virtual": 0,
        "is_on": 1,
        "sub_list": [
          {
            "id": 574,
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
      };
    }
  };
</script>
