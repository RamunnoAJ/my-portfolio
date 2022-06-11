<template>
  <footer class="footer">
    <div class="container">
      <div class="icons">
        <div>
          <img src="/logo.png" alt="image of the logo">
        </div>
        <div>
          <a href="https://github.com/RamunnoAJ" target="_blank"><i class="fa-brands fa-github"></i></a>
          <a href="https://www.linkedin.com/in/aramunno-frontend-vue/" target="_blank"><i
              class="fa-brands fa-linkedin"></i></a>
          <a href="https://www.instagram.com/agustinram1/" target="_blank"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>
      <hr>
      <p class="copyright"> Copyright © 2022 Agustin Ramunno. All Rights Reserved.</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: var(--color-background);
}

.icons {
  display: flex;
  text-align: center;
  justify-content: space-around;
  align-items: center;
}

.icons a {
  color: var(--color-primary);
  margin: 0.5em;
  font-size: var(--font-size-st-l);
  transition: 0.5s ease all;
}

.icons a:hover {
  color: var(--color-secondary);
}

img {
  text-align: left;
  width: 50px;
  height: 50px;
}

hr {
  background: var(--color-primary);
  border: none;
  height: 1.5px;
  margin: 1.5em;
}

.copyright {
  text-align: right;
  margin-right: 2em;
  font-size: var(--font-size-st-xs);
}

.container {
  margin: 0 auto;
  max-width: 1344px;
  text-align: center;
}
</style>