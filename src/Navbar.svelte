<script>
  import { capitalize } from "./utils";
  import Logo from "./Logo.svelte";

  const sections = ["about", "projects", "résumé", "contact"];
</script>

<nav>
  <Logo />
  <div>
    {#each sections as section}
      <a href={"#" + section}>{capitalize(section)}</a>
    {/each}
  </div>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    font-family: "Iosevka", monospace;
    position: fixed;
    padding: 0 1em;
    width: 95%;
    top: 2em;
  }

  div {
    margin-top: 1em;
  }

  a {
    color: #000000;
    display: inline-block;
    font-size: 1.5em;
    margin: 0 0.5em;
    text-decoration: underline 3px;
    text-decoration-color: #ffffff;
    transition: text-decoration-color 0.75s;
  }

  a:hover {
    text-decoration-color: indianred;
  }
</style>
