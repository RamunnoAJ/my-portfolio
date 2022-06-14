<template>
  <section class="container section">
    <h1 class="title">My Projects:</h1>
    <div class="website-card card-1">
      <div class="inner">
        <h2 class="title">Ramunno & Asociados</h2>
        <p>An app designed for a lawyer bussiness, an online resource to connect to a law firm in the city. <br>
          • HTML - CSS - JavaScript</p>
        <ul>
          <li>
            <a href="https://github.com/RamunnoAJ/ramunnoyasociados" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/Github.svg" alt="github icon">
              </figure>
            </a>
          </li>
          <li>
            <a href="https://ramunnoaj.github.io/ramunnoyasociados/" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/web.svg" alt="web icon">
              </figure>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="website-card card-2">
      <div class="inner">
        <h2 class="title">Tequierumi</h2>
        <p>An in develop e-commerce site created for selling crochet fabrics of little figures.<br>
          • HTML - CSS - JavaScript</p>
        <ul>
          <li>
            <a href="https://github.com/RamunnoAJ/tequierumi" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/Github.svg" alt="github icon">
              </figure>
            </a>
          </li>
          <li>
            <a href="https://ramunnoaj.github.io/tequierumi/" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/web.svg" alt="web icon">
              </figure>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="website-card card-3">
      <div class="inner">
        <h2 class="title">Personal portfolio</h2>
        <p>My personal portfolio, featuring information about me and some projects I've worked on.<br>
          • Vue.js - Vite - BulmaUI</p>
        <ul>
          <li>
            <a href="https://github.com/RamunnoAJ/my-portfolio" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/Github.svg" alt="github icon">
              </figure>
            </a>
          </li>
          <li>
            <a href="" target="_blank">
              <figure class="image is-32x32">
                <img src="../assets/icons/web.svg" alt="web icon">
              </figure>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  margin-top: var(--padding-l-v);
  margin-inline: auto;
}

.title {
  color: var(--color-secondary);
  font-size: var(--font-size-d-l);
  text-align: center;
}

.website-card {
  height: 50vh;
  width: 90%;
  margin-inline: auto;
  position: relative;
  padding: var(--padding-m-v) var(--padding-m-h);
  background-color: var(--color-secondary);
  box-sizing: border-box;
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: flex-end;
  border-radius: 10px;
  margin-block: var(--padding-l-v);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.card-1 {
  background-image: url('../assets/ramunnoyasociados.png');
}

.card-2 {
  background-image: url('../assets/tequierumi.png');
}

.card-3 {
  background-image: url('../assets/personal-portfolio.png');
}

.inner {
  width: 40%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: var(--color-background);
  box-sizing: border-box;
  padding: var(--padding-s-v) var(--padding-s-h);
  border-radius: 10px;
}

.inner .title {
  font-size: var(--font-size-st-l);
}

p {
  font-size: var(--font-size-d-xxs);
}

ul {
  align-self: flex-end;
  display: flex;
}

li {
  padding: 0 0 0 var(--padding-xxs-h);
}

.image {
  transition: all .5s ease;
}

.image:hover {
  transform: translateY(-5px);
}

@media (max-width: 768px) {
  .inner {
    width: 100%;
  }

  .inner .title {
    font-size: var(--font-size-d-m);
  }

  .website-card {
    margin-block: var(--padding-s-v);
  }

  p {
    font-size: var(--font-size-d-xs);
  }
}
</style>