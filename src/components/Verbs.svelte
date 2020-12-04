<script>
  import Verb from './Verb';
  import Search from './Search';
  export let verbs = [];
  let searchVerbs = verbs;

  const handleSearch = (event) => {
    const value = event.target.value;
    searchVerbs = verbs.filter(verb =>
      verb.simpleForm.toLowerCase().includes(value.toLowerCase())
    );
  }
</script>

<style>
  .Verbs {
    background-color: white;
    border-radius: 6px;
    border: 1px solid rgba(44,43,55, 0.2);
    margin: 1em 0;
  }
  .Verbs-header {
    display: grid;
    grid-template-columns: 30px 30px 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-gap: 1em;
    text-align: center;
  }
</style>

<Search handleSearch={handleSearch} />

<div class="Verbs">
  <div class="Verbs-header">
    <div>
      <h3>ID</h3>
    </div>
    <div>
      <h3>Type</h3>
    </div>
    <div>
      <h3>Simple Form</h3>
    </div>
    <div>
      <h3>Third Person</h3>
    </div>
    <div>
      <h3>Simple Past</h3>
    </div>
    <div>
      <h3>Past Participle</h3>
    </div>
    <div>
      <h3>Gerund</h3>
    </div>
    <div>
      <h3>Meaning</h3>
    </div>
  </div>
  <div class="Verbs-items">
    {#each searchVerbs as verb}
      <Verb verb={verb} />
    {/each}
  </div>
</div>