<script>
  import { fade, scale } from "svelte/transition";
  let show = false;
</script>

<label>
  Toggle
  <input type="checkbox" bind:checked={show} />
</label>

<hr />
{#if show}
  <h1 in:scale out:fade>My name is Nefe James</h1>
{/if}
