<script setup>
import { ref } from 'vue';
import ChildComponentModel from './ChildComponentModel.vue';

const sharedMessage = ref('');
</script>

<template>
    <ChildComponentModel v-model="sharedMessage" />
    <p>Huidig bericht: {{ sharedMessage }}</p>
</template>