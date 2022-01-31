<template>
    <footer>
        <div class="footer-links">
            <a href="">Advertising</a>
            <a href="">Business</a>
            <a href="">How Search Works</a>
        </div>

        <div class="footer-links">
            <a href="">Carbon neutral since 2007</a>
        </div>

        <div class="footer-links">
            <a href="">Privacy</a>
            <a href="">Terms</a>
            <a href="">Settings</a>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'landing-footer'
}
</script>

<style scoped>
    footer {
        display: grid;
        grid-template-columns: repeat(3, 1fr);

        width: 100%;
        height: 47px;

        background-color: #f2f2f2;
    }
    footer a {
        color: #70757a;
        font-size: 14px;
        font-family: Roboto, arial, sans-serif;
        text-decoration: none;
    }
    footer a:hover {
        text-decoration: underline;
    }

    .footer-links {
        display: flex;
        align-items: center;
        gap: 2rem;

        margin: 0 1rem;
    }
    .footer-links:nth-of-type(2) {
        justify-content: center;
    }
    .footer-links:nth-of-type(3) {
        justify-content: flex-end;
    }
</style>