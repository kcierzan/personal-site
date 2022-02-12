<script>
    import {createEventDispatcher} from "svelte";

    const dispatch = createEventDispatcher();

    export let visible;

    function navigate(page) {
        const nulled = {
            about: false,
            projects: false,
            resume: false,
            contact: false
        }
        dispatch('navigate', {
            ...nulled, [page]: true
        })
    }

</script>

<nav>
    <a href="" on:click|preventDefault={() => navigate("about")} class:selected="{visible.about}">
        About
    </a>
    <a href="" on:click|preventDefault={() => navigate("projects")} class:selected="{visible.projects}">
        Projects
    </a>
    <a href="" on:click|preventDefault={() => navigate("resume")} class:selected="{visible.resume}">
        Résumé
    </a>
    <a href="" on:click|preventDefault={() => navigate("contact")} class:selected="{visible.contact}">
        Contact
    </a>
</nav>

<style>
    nav {
        font-family: "Iosevka", monospace;
        position: absolute;
        right: 5%;
        top: 5%;
    }

    a {
        color: #000000;
        display: inline-block;
        font-size: 1.5em;
        margin: 0 .2em 0 .2em;
        text-decoration: underline 3px;
        text-decoration-color: #ffffff;
        transition: text-decoration-color 0.75s;
    }

    a.selected {
        text-decoration: underline 3px;
        text-decoration-color: #000;
    }

    a:hover {
        text-decoration-color: indianred;
    }

</style>