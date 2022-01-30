<template>
    <form id="search-form">
        <div id="input-container">
            <button id="search-icon" type="submit"></button>
            <input type="search" v-model="value" v-on:input="search" />
            <button id="voice-button" type="button"></button>
        </div>
        <ul>
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

    data: function() {
        return {
            value: ''
        }
    },
    
    methods: {
        search: function() {
            console.log(this.value);
        }
    }
}
</script>

<style scoped>
#input-container {
    display: grid;
    grid-template-columns: 44px 1fr 44px;

    height: 44px;
    width: auto;
    max-width: 584px;
    border: 1px solid #dfe1e5;
    border-radius: 24px;

    background-color: white;

    transition: box-shadow ease 300ms;
}
#input-container:hover, #input-container:focus-within {
    box-shadow: 0 1px 6px rgb(32 33 36 / 28%);
}

#search-icon, #voice-button {
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
</style>