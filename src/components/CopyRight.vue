<template>
  <footer>
    <p>
      This game owned by
      <a href="https://www.facebook.com/louis.long.1004">Long Louis</a>
      in Vue 3 course
    </p>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
footer {
  position: fixed;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9;
}

footer p {
  font-size: 1.4rem;
  color: var(--light);
}

footer a {
  transition: 0.3s linear;
  color: yellow;
}

footer a:hover {
  color: greenyellow;
}
</style>
