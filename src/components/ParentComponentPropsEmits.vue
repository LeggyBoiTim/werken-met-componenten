<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponentPropsEmits.vue';

const message = ref('Test');

const handleMessage = (content) => {
    message.value = content;
}
</script>

<template>
    <ChildComponent :message="message" @sendMessage="handleMessage" />
</template>