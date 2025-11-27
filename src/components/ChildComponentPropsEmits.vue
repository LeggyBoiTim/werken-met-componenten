<script setup>
defineProps({
    message: String,
});

const emit = defineEmits(['sendMessage']);

const sendMessageEvent = () => {
    emit('sendMessage', 'Nieuw bericht');
}
</script>

<template>
    <div>
        <h3>{{ message }}</h3>
    </div>

    <div>
        <button @click="sendMessageEvent">Verzend Bericht</button>
    </div>
</template>