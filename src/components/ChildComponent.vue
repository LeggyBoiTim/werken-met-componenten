<script setup>
defineProps({
    message: String,
});

const emit = defineEmits(['updateMessage']);

const emitEvent = () => {
    emit('updateMessage', 'Nieuw bericht');
}
</script>

<template>
    <div>
        <h3>{{ message }}</h3>
    </div>

    <div>
        <button @click="emitEvent">Verzend Bericht</button>
    </div>
</template>