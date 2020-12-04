<script>
  export let handleSearch;
</script>

<style>
  input {
    width: calc(100% - 22px);
    margin: 0 0 10px 0;
    border: none;
    outline: none;
    padding: 10px;
    font-size: 14px;
    color: #2C2B37;
    border: 1px solid rgba(0,0,0,0.3);
    border-radius: 4px;
  }
</style>

<div class="Search">
  <input
    type="text"
    placeholder="Search Verb"
    on:keyup={event => handleSearch(event)} />
</div>