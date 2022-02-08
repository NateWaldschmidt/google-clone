<template>
    <button v-bind:type="buttonType">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'landing-button',

    props: {
        buttonType: {
            default: 'button',
            type: String
        }
    }
}
</script>

<style scoped>
    button {
        cursor: pointer;

        min-width: 54px;
        height: 36px;
        margin: 0.5rem 0.25rem;
        padding: 0 1rem;
        border: 1px solid #f8f9fa;
        border-radius: 4px;

        background-color: #f8f9fa;

        color: #3c4043;
        font-size: 14px;
        line-height: 27px;

        transition: all ease 300ms;
    }

    button:hover {
        border: 1px solid #dadce0;
        box-shadow: 0 1px 1px rgb(0 0 0 / 10%);
    }

    button:focus {
        border: 1px solid #4285f4;
    }
</style>