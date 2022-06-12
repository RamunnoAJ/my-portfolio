<template>
  <section class="hero is-fullheight">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">Agustin Ramunno</h1>
        <h2 class="subtitle">Vue.js Developer</h2>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-image: url('../assets/background.jpg');
  background-position: center;
  background-size: cover;
}

.title {
  color: var(--color-terciary);
  font-size: var(--font-size-d-l);
  font-weight: 700;
  line-height: 1.4;
}

.subtitle {
  color: var(--color-terciary);
  font-weight: 500;
  font-size: var(--font-size-d-xs);
}

.container {
  text-align: left;
}
</style>
