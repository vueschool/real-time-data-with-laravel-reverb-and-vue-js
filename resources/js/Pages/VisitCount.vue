<script setup>
import { ref } from "vue";
const count = ref(0);
Echo.channel("hello-world").listen("HelloWorld", (e) => {
    count.value++;
});
</script>
<template>
    <div>The visit count is {{ count }}</div>
</template>
