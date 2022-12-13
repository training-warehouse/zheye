<template>
  <div>
    <global-header :user="user"></global-header>
    <div class="container">
      <column-list :list="list"></column-list>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from '@/components/ColumnList.vue'
import GlobalHeader, { UserProps } from '@/components/GlobalHeader.vue'

const user: UserProps = {
  isLogin: true,
  name: 'liaokong'
}

const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: '这是test1的专栏，又一段忧思的简介，棒棒哒'
  },
  {
    id: 2,
    title: 'test2的专栏',
    description: '这是test2的专栏，又一段忧思的简介，棒棒哒',
    avatar: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.qqan.com%2Fup%2F2021-4%2F16189694769878569.jpg&refer=http%3A%2F%2Fp.qqan.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1673534456&t=09b62e64119447b70a3c6ea4164a0ff3'
  },
  {
    id: 3,
    title: 'test2的专栏',
    description: '这是test2的专栏，又一段忧思的简介，棒棒哒',
    avatar: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.qqan.com%2Fup%2F2021-4%2F16189694769878569.jpg&refer=http%3A%2F%2Fp.qqan.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1673534456&t=09b62e64119447b70a3c6ea4164a0ff3'
  },
  {
    id: 4,
    title: 'test2的专栏',
    description: '这是test2的专栏，又一段忧思的简介，棒棒哒',
    avatar: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.qqan.com%2Fup%2F2021-4%2F16189694769878569.jpg&refer=http%3A%2F%2Fp.qqan.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1673534456&t=09b62e64119447b70a3c6ea4164a0ff3'
  },
  {
    id: 5,
    title: 'test2的专栏',
    description: '这是test2的专栏，又一段忧思的简介，棒棒哒',
    avatar: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.qqan.com%2Fup%2F2021-4%2F16189694769878569.jpg&refer=http%3A%2F%2Fp.qqan.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1673534456&t=09b62e64119447b70a3c6ea4164a0ff3'
  },
  {
    id: 6,
    title: 'test2的专栏',
    description: '这是test2的专栏，又一段忧思的简介，棒棒哒',
    avatar: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.qqan.com%2Fup%2F2021-4%2F16189694769878569.jpg&refer=http%3A%2F%2Fp.qqan.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1673534456&t=09b62e64119447b70a3c6ea4164a0ff3'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    GlobalHeader,
    ColumnList
  },
  setup () {
    return {
      list: testData,
      user
    }
  }
})
</script>

<style>
</style>
