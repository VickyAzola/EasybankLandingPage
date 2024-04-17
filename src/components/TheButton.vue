<script setup>

defineProps(['text'])

</script>

<template>
    <button class="baseButton">
        {{ text }}
    </button>
</template>

<style scoped>
.baseButton {
    padding: .7rem 1.8rem;
    margin: 1rem 0;
    color: white;
    border-radius: 2rem;
    background: linear-gradient(90deg, hsl(136, 65%, 51%), hsl(192, 70%, 51%));
}

.baseButton:hover {
    background: linear-gradient(90deg, hsl(136, 79%, 65%), hsl(192, 81%, 70%));
    cursor: pointer;
}
</style>