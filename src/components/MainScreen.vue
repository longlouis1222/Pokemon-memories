<template>
  <div class="screen">
    <h1>POKE MEMORIES</h1>
    <h2>Select mode to start game</h2>
    <div class="modes">
      <button @click="onStart(16)">
        <span>4x4</span>
        <span>Easy</span>
      </button>
      <button @click="onStart(36)">
        <span>6x6</span>
        <span>Normal</span>
      </button>
      <button @click="onStart(64)">
        <span>8x8</span>
        <span>Hard</span>
      </button>
      <button @click="onStart(100)">
        <span>10x10</span>
        <span>Insane</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    onStart(totalOfBlocks) {
      this.$emit("onStart", { totalOfBlocks });
    },
  },
};
</script>

<style scoped>
.screen {
  width: 100%;
  height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  background-color: var(--dark);
  color: var(--light);

  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
}

.screen h1 {
  font-size: 4.5rem;
}

.screen h2 {
  font-size: 1.8rem;
}

.modes {
  display: flex;
}

.modes button {
  width: 150px;
  height: 150px;
  border: 1px solid var(--light);
  border-radius: 10px;
  margin: 2rem 1rem 1rem;

  background-color: transparent;
  color: var(--light);
  font-family: var(--font);
  font-size: 1.5rem;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  transition: background 0.3s linear;
  cursor: pointer;
}

.modes button:hover {
  background-color: var(--light);
  color: var(--dark);
}

.modes button span:first-child {
  font-size: 2rem;
  margin-bottom: 0.5rem;
}
</style>
