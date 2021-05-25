<script>
  import BitFumesTween from "./1BitFumesTween.svelte";
  import OfficialTweened from "./2OfficialTweened.svelte";
  import BitFumesSpring from "./3BitFumesSpring.svelte";
  import BitFumesTransition from "./4BitFumesTransition.svelte";
  import DCodeTransition from "./5DCodeTransition.svelte";
  import CustomTransition from "./6CustomTransition.svelte";
  import AnimateDirective from "./7AnimateDirective.svelte";
  //unlike with Reeact,when importing components in Svelte,you have to add the .svelte file ext
</script>

<main>
  <!-- <BitFumesTween /> -->
  <!-- <OfficialTweened /> -->
  <!-- <BitFumesSpring /> -->
  <!-- <BitFumesTransition /> -->
  <!-- <DCodeTransition /> -->
  <!-- <CustomTransition /> -->
  <AnimateDirective />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  :global(h1) {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
