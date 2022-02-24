<template>
    <button class="btn-template" :class="{ white: theme === 'white' }">
        <p>{{ text }}</p>
    </button>
</template>

<script>
export default {
    props: ['text', 'theme'],
};
</script>

<style scoped>
.btn-template {
    background: black;
    color: #f1f1f1;
    padding: 13px 40px;
    border-radius: 40px;
    margin: 0 5px;
    border: none;
    transition-duration: 0.08s;
    font-size: 12px;
    letter-spacing: 2px;
    cursor: pointer;
}
button:hover {
    transform: scale(1.05);
}

.btn-template.white {
    background: white;
    color: black;
}
</style>
