<script>
  export let verb = {};
</script>

<style>
  .Verb-items {
    display: grid;
    grid-template-columns: 30px 30px 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-gap: 1em;
    border-top: 1px solid rgba(44,43,55,0.2);
    text-align: center;
  }
  h3 {
    padding: 0 1em;
    color: rgba(44, 43, 55, 0.7);
    font-size: 14px;
  }
</style>

<div class="Verb">
  <div class="Verb-items">
    <div class="Verb-item">
      <h3>{verb.id}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.type}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.simpleForm}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.thirdPerson}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.simplePast}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.pastParticiple}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.gerund}</h3>
    </div>
    <div class="Verb-item">
      <h3>{verb.meaning}</h3>
    </div>
  </div>
</div>