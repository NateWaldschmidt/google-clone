<template>
    <main>
        <landing-search />
        <landing-button type="submit">Google Search</landing-button>
    </main>
</template>

<script>
import LandingButton from '../components/landing-button.vue';
import LandingSearch from '../components/landing-search.vue';

export default {
    name: 'IndexPage',

    components: {
        LandingButton,
        LandingSearch
    },

    data: function() {
        return {
            value: 'This is the inputted value.'
        }
    },

    methods: {
        log: function() {
            console.log(this.value);
        }
    }
}
</script>

<style scoped>
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    label {
        display: flex;
        flex-direction: column;
    }
</style>