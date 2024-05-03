<script setup>
defineProps(['value']);  // 親コンポーネントから子に落ちてくる設定。変数を定義しておくと使える
</script>

<template>
    <label class="block font-medium text-sm text-gray-700">
        <span v-if="value">{{ value }}</span>
        <span v-else><slot /></span>
    </label>
</template>
