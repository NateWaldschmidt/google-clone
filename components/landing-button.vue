<template>
    <button v-bind:type="type">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'landing-button',

    props: {
        type: 'button'
    }
}
</script>

<style scoped>
    button {
        cursor: pointer;

        min-width: 54px;
        margin: 0.5rem 0.25rem;
        padding: 0 1rem;
        border: 1px solid #f8f9fa;
        border-radius: 4px;

        background-color: #f8f9fa;

        line-height: 27px;
    }
</style>