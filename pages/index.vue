<template>
    <div id="google-clone">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
        <landing-header />
        <main>
            <h1>
                <span class="color-blue">N</span><span class="color-red">a</span><span class="color-yellow">t</span><span class="color-blue">h</span><span class="color-green">a</span><span class="color-red">n</span><span class="color-blue">i</span><span class="color-red">e</span><span class="color-yellow">l</span>
            </h1>
            <landing-search />
            <div id="button-group">
                <landing-button buttonType="submit">{{ siteName }} Search</landing-button>
                <landing-button buttonType="submit">I'm Feeling Lucky</landing-button>
            </div>
        </main>
        <landing-footer />
    </div>
</template>

<script>
import LandingButton from '../components/landing-button.vue';
import LandingSearch from '../components/landing-search.vue';
import LandingFooter from '../components/landing-footer.vue';
import LandingHeader from '../components/landing-header.vue';

export default {
    name: 'IndexPage',

    components: {
        LandingButton,
        LandingSearch,
        LandingFooter,
        LandingHeader
    },

    data: function() {
        return {
            siteName: 'Google',
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
        justify-content: center;

        height: 100%;
    }
    main > * {
        position: relative;
        top: -13vh;
    }

    label {
        display: flex;
        flex-direction: column;
    }

    h1 {
        font-family: 'Poppins', sans-serif;
        font-size: 5rem;
        margin: 2rem 0;
    }
    .color-blue { color: #4285F4; }
    .color-red { color: #EA4335; }
    .color-yellow { color: #FBBC05; }
    .color-green { color: #34A853; }

    #button-group {
        margin-top: 1.5rem;
    }
</style>