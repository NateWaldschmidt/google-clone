<template>
    <header>
        <div class="header-link-group">
            <a href="https://about.google">
                About
            </a>
            <a href="https://store.google.com">
                Store
            </a>
        </div>
        <div class="header-link-group">
            <a href="https://mail.google.com">Gmail</a>
            <a href="https://www.google.com/imghp?hl=en&ogbl">Images</a>
            <button id="more-options" v-on:focus="hideApps = false" v-on:blur="hideApps = true">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                    <circle cx="3" cy="3" r="3" fill="#626368"/>
                    <circle cx="21" cy="3" r="3" fill="#626368"/>
                    <circle cx="21" cy="21" r="3" fill="#626368"/>
                    <circle cx="12" cy="12" r="3" fill="#626368"/>
                    <circle cx="3" cy="12" r="3" fill="#626368"/>
                    <circle cx="12" cy="3" r="3" fill="#626368"/>
                    <circle cx="21" cy="12" r="3" fill="#626368"/>
                    <circle cx="12" cy="21" r="3" fill="#626368"/>
                    <circle cx="3" cy="21" r="3" fill="#626368"/>
                </svg>
            </button>
            <button id="user-profile">N</button>
        </div>
        <aside id="application-container" v-bind:hidden="hideApps">
            <ul>
                <li>
                    <a href="">
                        <div class="app-logo"></div>
                        <span>App1</span>
                    </a>
                </li>
                <li>
                    <a href="">
                        <div class="app-logo"></div>
                        <span>App1</span>
                    </a>
                </li>
                <li>
                    <a href="">
                        <div class="app-logo"></div>
                        <span>App1</span>
                    </a>
                </li>
            </ul>
        </aside>
    </header>
</template>

<script>
export default {
    name: 'landing-header',

    data: function() {
        return {
            hideApps: true
        }
    }
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;

        height: 60px;

        font-family: Roboto, arial, sans-serif;
        font-size: 14px;
    }

    .header-link-group {
        display: flex;
        align-items: center;
        gap: 1rem;

        margin: 1rem;
    }

    .header-link-group > * {
        padding: 0.25rem;

        color: #202124;
        text-decoration: none; /* Removes the underlines for links. */
    }

    /* The links in the second group are slightly smaller text. */
    .header-link-group:nth-of-type(2) {
        font-size: 13px;
    }

    .header-link-group > a:hover, .header-link-group > a:active {
        text-decoration: underline;
    }

    #more-options, #user-profile {
        cursor: pointer;

        width: 32px;
        height: 32px;

        border: none;
        border-radius: 100%;
    }

    #more-options:hover, #user-profile:hover {
        outline: 4px solid rgba(60,64,67,0.08);
    }

    #more-options:focus, #user-profile:focus {
        outline: 4px solid rgba(95,99,104,0.24);
    }

    #more-options {
        display: flex;
        justify-content: center;
        align-items: center;

        position: relative;

        background-color: transparent;
    }
    #more-options > svg {
        width:  16px;
        height: 16px;
    }
    #more-options:hover {
        background-color: rgba(60,64,67,0.08);
    }
    #more-options:focus {
        background-color: rgba(95,99,104,0.24);
    }

    /* The profile image button. */
    #user-profile {
        background-color: #f94144;

        color: white;
        font-weight: 500;
        font-size: 1.125rem;
    }

    #application-container {
        position: absolute;
        top: calc(60px + 1rem);
        right: 1rem;

        height: 438px;
        padding: 1rem;
        border: 1px solid rgba(0,0,0,0.2);
        border-radius: 8px;

        box-shadow: 0 1px 6px rgb(32 33 36 / 28%);

        overflow-y: scroll;
    }
    #application-container > ul {
        display: grid;
        grid-template-columns: repeat(3, 84px);
        grid-auto-rows: 84px;
        gap: 1rem;

        list-style: none;

        margin: 0;
        padding: 0;
    }
    #application-container > ul > li {
        border-radius: 8px;
        box-sizing: border-box;

        background-color: white;
    }
    #application-container > ul > li:hover, #application-container > ul > li:focus {
         background-color: #e8f0fe;
    }
    #application-container > ul > li > a {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        
        width: 100%;
        height: 100%;
        padding: 5px;
        box-sizing: border-box;

        color: #202124;
        text-decoration: none;
    }
    .app-logo {
        width: 44px;
        height: 44px;
        border-radius: 100%;

        background-color: #f94144;
    }
</style>