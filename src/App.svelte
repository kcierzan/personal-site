<script>
    import Navbar from "./Navbar.svelte";
    import About from "./About.svelte";
    import Projects from "./Projects.svelte";
    import Section from "./Section.svelte";

    export let name;

</script>

<Navbar/>
<main>
    <div class="scroll-container">
        <Section id="splash">
            <h1>Kyle <span>Cierzan</span></h1>
            <h2>Software Engineer</h2>
        </Section>
        <Section id="about">
            <About/>
        </Section>
        <Section id="projects">
            <Projects/>
        </Section>
        <Section id="résumé">
            <h3>My résumé</h3>
        </Section>
        <Section id="contact">
            <h3>Contact me</h3>
        </Section>
    </div>
</main>

<style>

    .scroll-container {
        height: 100vh;
        overflow-y: scroll;
        scroll-snap-type: y mandatory;
        scroll-behavior: smooth;
    }

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
