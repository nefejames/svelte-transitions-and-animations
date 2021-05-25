<script>
  import { fade, blur, fly, slide, scale } from "svelte/transition";
  import { quintOut } from "svelte/easing";

  const book1 = "./images/book1";
  const book2 = "./images/book2";
  const book3 = "./images/book3";

  //consider an article on how to make carousel slider with Sveltejs

  let books = [
    "https://source.unsplash.com/collection/190727",
    "https://source.unsplash.com/user/erondu/likes",
    "https://source.unsplash.com/user/erondu",
  ];

  let activeIndex = 0;

  setInterval(() => {
    let next = activeIndex + 1;
    activeIndex = next == 3 ? 0 : next;
  }, 1000);
</script>

<section style="display:flex;justify-content:center">
  {#each books as book, i}
    {#if activeIndex === i}
      <img
        transition:scale={{ delay: 250, duration: 300, easing: quintOut }}
        style="position:absolute"
        src={book}
        width="500"
        height="300"
        alt=""
      />
    {/if}
  {/each}
</section>
