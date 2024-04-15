<script setup>
import { Inertia } from '@inertiajs/inertia' // 古い書き方

// コントローラーから渡ってくるオブジェクト専用のメソッドdefineProps()
  defineProps({
    id: String,
    blog: Object
  })

const deleteConfirm = (id) => {
  console.log(id)
  Inertia.delete(`/inertia/${id}`, {
    onBefore: () => confirm('本当に削除しますか？')
  })

}
</script>

<template>
  {{ id }}<br>
  {{ blog.title }}
  <button @click="deleteConfirm(blog.id)">削除</button>
</template>
