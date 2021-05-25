<script>
  import { tweened } from "svelte/motion";
  import { quartInOut } from "svelte/easing";

  let src = "./images/pear.jpg";
  //images have to be put inside a IMAGES folder in the PUBLIC directory in Svelte

  const width = tweened(100, {
    duration: 2000,
    easing: quartInOut,
  });

  function handleClick() {
    width.set(150);
  }
</script>

<button on:click={handleClick}>Animate</button>
<br />

<img {src} width={$width} alt="" />
