<template>
    <form id="search-form">
        <div id="input-container">
            <button id="search-icon" type="submit"></button>

            <input
            type="search"
            v-model="searchValue"
            v-on:input="search"
            v-on:focus="hideSearchesResults = false"
            v-on:blur="hideSearchesResults = true"
            />
            
            <button id="voice-button" type="button"></button>
        </div>
        <ul id="searches-results" v-bind:hidden="hideSearchesResults">
            <li>
                <article>
                    <a href="">Search Result 1</a>
                </article>
            </li>
            <li>
                <article>
                    <a href="">Search Result 1</a>
                </article>
            </li>
            <li>
                <article>
                    <a href="">Search Result 1</a>
                </article>
            </li>
            <li>
                <article>
                    <a href="">Search Result 1</a>
                </article>
            </li>
            <li>
                <article>
                    <a href="">Search Result 1</a>
                </article>
            </li>
        </ul>
    </form>
</template>

<script>
export default {
    name: 'landing-search',

    props: {
        searchValue: ''
    },

    data: function() {
        return {
            // Toggles the showing and hiding of previous searches.
            hideSearchesResults: true
        }
    },
    
    methods: {
        search: function() {
            console.log(this.searchValue);
        }
    }
}
</script>

<style scoped>
#search-form {
    /* Allows the overflow of the search results.  This
    positions them properly beneath the search input. */
    max-height: 44px;
    overflow: visible;

    /* Allows overlaying of the search results. */
    z-index: 1;
}
#input-container {
    display: grid;
    grid-template-columns: 44px 1fr 44px;

    height: 44px;
    max-width: 584px;
    border: 1px solid #dfe1e5;
    border-radius: 24px;

    background-color: white;

    transition: box-shadow ease 300ms;
}
#input-container:focus-within {
    border-radius: 24px 24px 0 0;
}
#input-container:hover, #input-container:focus-within {
    box-shadow: 0 1px 6px rgb(32 33 36 / 28%);
}

#search-icon, #voice-button {
    cursor: pointer;

    margin: 0.75rem;
    border: none;
    border-radius: 100%;

    background-color: tomato;
}

input[type=search] {
    border: none;
    outline: none;

    background-color: transparent;
    
    color: rgba(0,0,0,0.87);
    font-size: 1rem;
}

#searches-results {
    list-style: none;

    margin: 0;
    padding: 0.5rem 1.5rem;
    border-radius: 0 0 24px 24px;

    background-color: white;
    box-shadow: 0 1px 6px rgb(32 33 36 / 28%);
}
</style>