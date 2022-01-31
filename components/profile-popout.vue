<template>
    <aside id="profile-container">
        <section id="profile-top">
            <div id="big-profile-icon">
                <span>N</span>
            </div>
            <div class="profile-group">
                <p id="profile-title">Nathaniel Waldschmidt</p>
                <address id="profile-email">Nathaniel.Waldsch@gmail.com</address>
            </div>
            <a id="profile-email-contact" href="mailto:nathaniel.waldsch@gmail.com">Contact Nathaniel</a>
        </section>

        <a id="profile-projects" href="">View more projects</a>

        <div id="profile-phone-container">
            <a id="profile-phone-link" href="tel:16309011086">Call Me</a>
        </div>
    </aside>
</template>

<script>
export default {
    name: 'profile-popout'
}
</script>

<style scoped>
    #profile-container {
        position: absolute;
        top: calc(60px + 1rem);
        right: 1rem;
        
        width: 356px;
        border: 1px solid rgba(0,0,0,0.2);
        border-radius: 8px;
        box-sizing: border-box;

        box-shadow: 0 1px 6px rgb(32 33 36 / 28%);

        overflow: hidden;
    }
    #profile-container[hidden] {
        display: none;
    }

    #profile-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
    }

    #profile-top {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;

        padding: 1rem;
    }

    #big-profile-icon {
        display: flex;
        justify-content: center;
        align-items: center;

        width: 80px;
        height: 80px;
        border-radius: 100%;

        background-color: #f94144;

        color: white;
        font-size: 2.5rem;
        font-weight: 500;
    }

    #profile-title {
        margin: 0;

        color: #202124;
        font: 500 16px/22px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
        letter-spacing: 0.29px;
    }

    .profile-group {
        text-align: center;
    }

    #profile-email {
        margin: 0;

        color: #5f6368;
        font-style: normal;
        font: 400 14px/19px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
    }

    #profile-email-contact {
        padding: 8px 16px;
        border: 1px solid #dadce0;
        border-radius: 100px;

        color: #3c4043;
        font: 500 14px/16px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
        text-decoration: none;

        transition: all ease 300ms;
    }
    #profile-email-contact:hover {
        background-color: #f7f8f8;
    }

    #profile-email-contact:active {
        background-color: #e8e8e9;
        border-color: transparent;
        box-shadow: 0 1px 2px 0 rgb(60 64 67 / 30%), 0 2px 6px 2px rgb(60 64 67 / 15%);
    }

    #profile-projects {
        width: 100%;
        padding: 14px 41px;
        box-sizing: border-box;

        color: #3c4043;
        font: 500 14px/16px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
        text-decoration: none;
        letter-spacing: 0.25px;
        border-top: 1px solid rgba(0,0,0,.1);
        border-bottom: 1px solid rgba(0,0,0,.1);

        transition: all ease 300ms;
    }
    #profile-projects:hover {
        background-color: #f7f8f8;
    }

    #profile-phone-container {
        margin-bottom: 1rem;
    }

    #profile-phone-link {
        display: block;

        margin: 0.125rem 0;
        padding: 8px 16px;
        border: 1px solid #dadce0;
        border-radius: 4px;

        color: #3c4043;
        font: 500 14px/16px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
        text-decoration: none;

        transition: all ease 300ms;
    }
    #profile-phone-link:hover {
        background-color: #f7f8f8;
    }
    #profile-phone-link:active {
        background-color: #e8e8e9;
        border-color: transparent;
        box-shadow: 0 1px 2px 0 rgb(60 64 67 / 30%), 0 2px 6px 2px rgb(60 64 67 / 15%);
    }
</style>