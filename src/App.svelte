<script>
    import Navbar from "./Navbar.svelte";
    export let name;

    let visible = {
        about: false,
        resume: false,
        projects: false,
        contact: false
    }
    function handleNavigate(event) {
        visible = event.detail;
    }
</script>

<Navbar on:navigate={handleNavigate} visible={visible}/>
<main>
    <div>
        <h1>Kyle <span>Cierzan</span></h1>
        <h2>Software Engineer</h2>
    </div>
</main>

<style>

    @font-face {
        font-family: "Iosevka";
        font-weight: normal;
        src: url('iosevka-ss14-medium.woff2') format('woff2');
    }

    @font-face {
        font-family: "Iosevka";
        font-weight: bold;
        src: url('iosevka-ss14-bold.woff2') format('woff2');
    }

    @font-face {
        font-family: "Iosevka Light";
        src: url('iosevka-ss14-light.woff2') format('woff2');
    }

    main {
        text-align: center;
        font-family: "Iosevka", monospace;
    }

    h1 {
        font-size: 5em;
        margin-top: 20%;
        font-weight: normal;
        font-family: "Iosevka Light", monospace;
        white-space: nowrap;
        margin-bottom: 0;
    }

    h2 {
        position: relative;
        font-family: "Iosevka Light", monospace;
        font-size: 1.2em;
        margin-top: 0;
        top: 0;
        left: 8em;
    }

    span {
        font-family: "Iosevka", monospace;
        font-weight: bold;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
