<template>
  <Navigation />
  <router-view v-slot="{ Component }">
    <transition name="fade">
      <component :is="Component" />
    </transition>
  </router-view>
  <Footer />

</template>

<script setup>
import Navigation from './components/Navigation.vue'
import Footer from './components/Footer.vue';

</script>

<style>
@import '@/assets/base.css';

.fade-enter-from,
.fade-leave-to {
  opacity: 1;
  transform: translateX(-500px);
}

.fade-enter-active {
  transition: 1s all ease;
}

a {
  text-decoration: none;
  transition: 0.4s;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
</style>
