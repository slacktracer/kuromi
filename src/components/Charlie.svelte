<script lang="ts">
  let pick = $state("none");

  function abc(event) {
    const x = event.target.id;

    pick = x;
  }
</script>

<div class="options">
  <div class="rock" class:selected={pick === "rock"} id="rock" onclick={abc}>
    👊
  </div>

  <div class="paper" class:selected={pick === "paper"} id="paper" onclick={abc}>
    🖐️
  </div>

  <div
    class="scissors"
    class:selected={pick === "scissors"}
    id="scissors"
    onclick={abc}
  >
    ✌️
  </div>
</div>

<h1>Você escolheu: <i>{pick}</i></h1>

<style>
  .options {
    font-size: 8rem;
  }

  .selected {
    outline: 10px solid firebrick;
  }
</style>
