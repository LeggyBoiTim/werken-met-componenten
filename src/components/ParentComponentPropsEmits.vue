<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponentPropsEmits.vue';

const message = 'Test';
const receivedMessage = ref('');

const handleMessage = (content) => {
    receivedMessage.value = content;
}
</script>

<template>
    <ChildComponent :message="message" @sendMessage="handleMessage" />
    <p>Bericht: {{ receivedMessage }}</p>
</template>