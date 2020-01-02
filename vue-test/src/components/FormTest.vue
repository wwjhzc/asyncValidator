<template>
  <div>
    form表单
    <hr />
    <k-form :model="model" :rules="rules" ref="kForm">
      <k-form-item label="用户名"  prop="username">
        <k-input v-model="model.username"></k-input>
      </k-form-item>
      <k-form-item label="密码" prop="password">
        <k-input type="password" v-model="model.password"></k-input>
      </k-form-item>
    </k-form>
  </div>
</template>
<script>
import KForm from "./KForm.vue";
import KInput from "./KInput.vue";
import KFormItem from "./KFormItem.vue";
export default {
  components: {
    KForm,
    KInput,
    KFormItem
  },
  data() {
    return {
      // 数据模型
      model: { username: "tom", password: "" },
      // 校验规则
      rules: {
        username: [{ required: true, message: "请输入用户名" }],
        password: [{ required: true, message: "请输入密码" }]
      }
    };
  }
};
</script>
<style>
</style>
