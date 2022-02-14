<script>

    function clickSvg() {
       location.href = "#splash"
    }

</script>

<svg on:click={clickSvg} width="140" height="130" viewBox="0 0 140 130" fill="black" xmlns="http://www.w3.org/2000/svg">
    <path fill-rule="evenodd" clip-rule="evenodd" d="M108.56 101C98.3094 110.181 84.7663 115.765 69.9184 115.765C55.0704 115.765 41.5274 110.181 31.277 101H70H108.56ZM117.225 91.2852C123.909 81.8482 127.837 70.3237 127.837 57.8823C127.837 25.9148 101.906 0 69.9184 0C37.9309 0 12 25.9148 12 57.8823C12 70.3682 15.9558 81.9307 22.6833 91.3864L36.546 76.0384C33.6461 70.6717 32 64.5281 32 58C32 37.0132 49.0132 20 70 20C90.9868 20 108 37.0132 108 58C108 64.5281 106.354 70.6717 103.454 76.0384L117.225 91.2852Z"/>
    <path d="M69.7362 125.924L26.5168 101.368L69.7362 101.368L112.956 101.368L69.7362 125.924Z"/>
    <path d="M69.736 53.5714L112.955 101.368H69.736H26.5166L69.736 53.5714Z"/>
</svg>

<style>
    svg {
        width: 90px;
        height: 90px;
        cursor: pointer;
        transition: fill 0.75s;
    }

    svg:hover {
        fill: indianred !important;
    }
</style>