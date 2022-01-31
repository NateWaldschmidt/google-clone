<template>
    <div id="google-clone">
        <landing-header />
        <main>
            <landing-search />
            <section>
                <landing-button type="submit">Google Search</landing-button>
                <landing-button type="submit">I'm Feeling Lucky</landing-button>
            </section>
        </main>
        <landing-footer />
    </div>
</template>

<script>
import LandingButton from '../components/landing-button.vue';
import LandingHeader from '../components/landing-header.vue';
import LandingSearch from '../components/landing-search.vue';

export default {
    name: 'IndexPage',

    components: {
        LandingButton,
        LandingSearch,
        LandingHeader
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

<style>
    /* Allows easier styling of the header. */
    body {
        height: 100vh;
        margin: 0;
    }
</style>

<style scoped>
    #google-clone {
        position: absolute;
        inset: 0 0 0 0;

        display: flex;
        flex-direction: column;
    }

    main {
        display: flex;
        flex-direction: column;
        align-items: center;

        height: 100%;
    }

    label {
        display: flex;
        flex-direction: column;
    }
</style>