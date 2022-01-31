<template>
    <div id="google-clone">
        <main>
            <img id="site-logo" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Google Logo">
            <landing-search />
            <div id="button-group">
                <landing-button type="submit">Google Search</landing-button>
                <landing-button type="submit">I'm Feeling Lucky</landing-button>
            </div>
        </main>
        <landing-footer />
    </div>
</template>

<script>
import LandingButton from '../components/landing-button.vue';
import LandingSearch from '../components/landing-search.vue';
import LandingFooter from '../components/landing-footer.vue';

export default {
    name: 'IndexPage',

    components: {
        LandingButton,
        LandingSearch,
        LandingFooter
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

    #site-logo {
        margin: 2rem 0;
    }

    #button-group {
        margin-top: 1.5rem;
    }
</style>