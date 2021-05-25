<script>
  import { spring } from "svelte/motion";

  let src = "./images/heart.jpg";

  const width = spring(100, {
    stiffness: 0.01,
    damping: 0.1,
  });

  const zoomIn = setInterval(() => {
    width.set(200);
  }, 300);

  const zoomOut = setInterval(() => {
    width.set(100);
  }, 600);
</script>

<img {src} alt="" width={$width} />
