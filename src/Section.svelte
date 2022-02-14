<script>
    export let id = "";
</script>

<section id="{id}">
    <div>
        <slot></slot>
    </div>
</section>

<style>
    section {
        height: 100vh;
        scroll-snap-align: center;
    }

    div {
        position: relative;
        top: 30%;
    }
</style>
