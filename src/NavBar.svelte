<script>
  import { flip } from "svelte/animate";
</script>

<div id="nav">
  <ul>
    <li><a href="#about">about</a></li>
    <li>projects</li>
  </ul>
</div>

<style>
  #nav {
    position: static;
  }
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    text-align: center;
  }
  li {
    display: inline;
    font-family: "Poppins", sans-serif;
  }
</style>
