<template>
  <section class="container">
    <div class="columns is-flex-direction-row-reverse is-align-items-center">
      <div class="column">
        <figure class="image is-square">
          <img src="../assets/foto carnet.jpg" class="is-rounded">
        </figure>
      </div>
      <div class="column is-two-thirds">
        <h1 class="title">
          A little <span>about me</span>
        </h1>
        <p>I'm a front-end developer with a hard focus on the simplicity of Vue.js and its libraries. <br>
          I'm from Argentina and of course, I love <a
            href="https://www.google.com/search?q=empanadas&client=opera-gx&sxsrf=ALiCzsYQXhWznk3beaJIyhKhiTYwsy-QAg:1655057035943&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjDgtf1v6j4AhWJspUCHd8GA-sQ_AUoAnoECAMQBA&biw=1879&bih=949&dpr=1#"
            target="_blank">empanadas</a> with the company of a good glass of <a
            href="https://www.google.com/search?q=Fernet+con+coca&tbm=isch&ved=2ahUKEwjc5-qHwKj4AhU1jZUCHQ5_BjUQ2-cCegQIABAA&oq=Fernet+con+coca&gs_lcp=CgNpbWcQAzIICAAQgAQQsQMyCwgAEIAEELEDEIMBMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQ6BwgAELEDEEM6BAgAEEM6CAgAELEDEIMBOgQIABADUOMHWOESYKsUaABwAHgAgAFWiAH5CJIBAjE2mAEAoAEBqgELZ3dzLXdpei1pbWfAAQE&sclient=img&ei=siqmYtxGtZrWxA-O_pmoAw&bih=949&biw=1879&client=opera-gx"
            target="_blank">fernet with cola.</a>
          <br>
          I love playing basketball and watching the NBA, I'm a huge fan of Kobe, his mamba mentality inspired me to
          do what I want.
        </p>
      </div>
    </div>
    <div class="skills section">
      <h1 class="title">The tools I use are:</h1>
      <div class="section">
        <ul class="tools">
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/JavaScript.svg" alt=""></figure>
            <p>JavaScript</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/vuejs.svg" alt=""></figure>
            <p>Vue.js</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/git.svg" alt=""></figure>
            <p>Git</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Github.svg" alt=""></figure>
            <p>GitHub</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/npm.svg" alt=""></figure>
            <p>NPM</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Adobexd.svg" alt=""></figure>
            <p>Adobe XD</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Bootstrap.svg" alt=""></figure>
            <p>Bootstrap</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Bulmaui.svg" alt=""></figure>
            <p>BulmaUI</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Firebase.svg" alt=""></figure>
            <p>Firebase</p>
          </li>
          <li>
            <figure class="image is-128x128"><img src="../assets/icons/Vite.svg" alt=""></figure>
            <p>Vite</p>
          </li>
        </ul>
      </div>

    </div>

  </section>
</template>

<style scoped>
.container {
  margin-top: var(--padding-xl-v);
  margin-inline: auto;
}

.columns {
  margin: 0 1em;
}

.column {
  max-width: 90%;
  margin: 0 auto;
}

.title {
  font-size: var(--font-size-d-l);
  color: var(--color-secondary);
}

p {
  font-size: var(--font-size-d-xs);
}

.title span {
  color: var(--color-primary);
}

.image {
  margin: 0 auto;
}

@media (min-width: 1050px) {
  .image {
    margin: 0;
  }
}

.skills {
  margin-top: var(--padding-l-v);
}

.skills.section {
  margin-inline: auto;
  margin-top: var(--padding-xl-v);
}

.skills .title {
  text-align: center;
  margin: 0 auto;
}

.section {
  margin-inline: auto;
}

.tools {
  display: flex;
  margin-top: var(--padding-m-v);
  margin-inline: auto;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: var(--padding-xxs-h);
  max-width: 60%;
}

@media (max-width: 800px) {
  .tools {
    max-width: 100%;
    gap: var(--padding-xs-v) 0;
  }
}

li>p {
  margin-top: var(--padding-xs-v);
  text-transform: uppercase;
  text-align: center;
}
</style>