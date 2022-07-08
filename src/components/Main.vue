<template>
  <section class="hero is-fullheight">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">Agustin Ramunno</h1>
        <h2 class="subtitle">Vue.js Developer</h2>
        <a href="../assets/agustin-ramunno-resume.pdf" target="_blank">
          <button type="button" class="button-main">Download
            CV</button>
        </a>
        <button type="button" class="button-main button-main-2"><a href="https://github.com/RamunnoAJ"
            target="_blank">See my work <i class="fa-brands fa-github"></i></a></button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-image: url('../assets/background.jpg');
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
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

.button-main {
  min-width: 130px;
  height: 40px;
  color: var(--color-terciary);
  padding: 5px 10px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  display: inline-block;
  outline: none;
  overflow: hidden;
  border-radius: 5px;
  border: none;
  background-color: var(--color-primary);
  margin: var(--padding-xs-v) var(--padding-xxs-h);
}

.button-main-2 {
  background-color: transparent;
  border: 1px solid var(--color-primary);
}

.button-main:hover {
  border-radius: 5px;
  padding-right: 24px;
  padding-left: 8px;
}

.button-main:hover::after {
  opacity: 1;
  right: 10px;
}

.button-main::after {
  content: "\00BB";
  position: absolute;
  opacity: 0;
  font-size: 20px;
  line-height: 40px;
  top: 0;
  right: -20px;
  transition: 0.4s;
}

a {
  color: var(--color-terciary);
  font-weight: bold;
}
</style>
