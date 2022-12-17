<template>
  <div class="container">
    <global-header :user="user"></global-header>
    <validate-form action="" @form-submit="onFormSubmit">
      <div class="mb-3">
        <label class="from-label">邮箱地址</label>
        <validate-input :rules="emailRules" v-model="emailVal" type="text" placeholder="请输入邮箱地址"></validate-input>
      </div>
      <div class="mb-3">
        <label class="form-label">密码</label>
        <validate-input :rules="passwordRules" v-model="passwordVal" type="password"
                        placeholder="请输入密码"></validate-input>
      </div>
      <template #submit>
        <button class="btn btn-danger">提交</button>
      </template>
    </validate-form>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
// import ColumnList, { ColumnProps } from '@/components/ColumnList.vue'
import GlobalHeader, { UserProps } from '@/components/GlobalHeader.vue'
import ValidateInput, { RulesProp } from '@/components/ValidateInput.vue'
import ValidateForm from '@/components/ValidateForm.vue'

const user: UserProps = {
  isLogin: true,
  name: 'liaokong'
}

export default defineComponent({
  name: 'App',
  components: {
    // ColumnList,
    GlobalHeader,
    ValidateInput,
    ValidateForm
  },
  setup () {
    const emailVal = ref('')
    const passwordVal = ref('')

    const emailRules: RulesProp = [
      {
        type: 'required',
        message: '邮箱地址不能为空'
      },
      {
        type: 'email',
        message: '邮箱地址格式不正确'
      }
    ]
    const passwordRules: RulesProp = [
      {
        type: 'required',
        message: '密码不能为空'
      }
    ]

    const onFormSubmit = (result: boolean) => {
      console.log(result)
    }

    return {
      // list: testData,
      user,
      emailRules,
      emailVal,
      passwordVal,
      passwordRules,
      onFormSubmit
    }
  }
})
</script>

<style>
</style>
