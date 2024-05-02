<script setup>
import Label from '@/Components/InputLabel.vue'
import Input from '@/Components/TextInput.vue'
import GuestLayout from '@/Layouts/GuestLayout.vue'

// 親の方で実行したい関数を定義しておく
// const emitTest = (e) => { console.log(e)}
const emitTest = e => console.log(e)
</script>

<template>
  <GuestLayout>
    <Label value="件名">タイトル</Label>
    <!-- <Label>ラベル</Label> -->
    <Input modelValue="初期値が入ります" @update:modelValue="emitTest"></Input>
  </GuestLayout>
</template>
