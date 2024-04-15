<script setup>
import { Link } from '@inertiajs/inertia-vue3'  // definePropsを書くときに書くのかな
import { ref } from 'vue'     // definePropsを書くときに書くのかな

defineProps({
  blogs: Array
})
</script>

<template>
  <div v-if="$page.props.flash.message" class="bg-blue-200">
    {{ $page.props.flash.message }}
  </div>
  <ul>
    <li v-for="blog in blogs" :key="blog.id">
      件名：<Link class="" :href="route('inertia.show', { id: blog.id })">ルートパラメーターのテストです{{ blog.title }}</Link><br>
      本文：{{ blog.content }}
    </li>
  </ul>
</template>
