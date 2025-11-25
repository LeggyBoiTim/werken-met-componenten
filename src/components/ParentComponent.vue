<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const message = 'Test';
const sentMessage = ref('');

const handleMessage = (newMessage) => {
    sentMessage.value = newMessage;
}
</script>



<template>
    <ChildComponent :message="message" @update-message="handleMessage" />
    <p>Bericht: {{ sentMessage }}</p>
</template>