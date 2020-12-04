<script>
  import { onMount } from 'svelte';
  import Header from '../components/Header.svelte';
  import Verbs from '../components/Verbs.svelte';
  import Footer from '../components/Footer.svelte';
  import data from "../initialState.json";
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');
  :global(body) {
    background-color: #f2f2f2;
    color: #2C2B37;
    font-family: 'Roboto', sans-serif;
  }
  .App {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }
</style>

<div class="App">
  <Header />
  {#if data}
    <Verbs verbs={data} />
  {/if}
  <Footer />
</div>
