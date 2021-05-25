<script>
  import { elasticInOut } from "svelte/easing";

  let isActive = true;

  const customTransition = () => {
    return {
      css: (t) => {
        return `
        transform: scale(${t});
        `;
      },
      easing: elasticInOut,
      duration: 2000,
    };
  };
</script>

<main>
  <button on:click={() => (isActive = !isActive)}>
    {#if isActive} Hide Box {:else} Show Box{/if}
  </button>

  {#if isActive}
    <div class="box" transition:customTransition />
  {/if}
</main>

<style>
  .box {
    background: blue;
    width: 150px;
    height: 150px;
    margin: 0 auto;
  }
</style>
