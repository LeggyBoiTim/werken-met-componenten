<script setup>
defineProps({
    message: String,
});

const emit = defineEmits(['sendMessage']);

const updateMessage = () => {
    emit('sendMessage', 'Nieuw bericht');
}
</script>

<template>
    <div>
        <h3>{{ message }}</h3>
    </div>

    <div>
        <button @click="updateMessage">Verzend Bericht</button>
    </div>
</template>