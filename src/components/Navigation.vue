<template>
  <header :class="{ 'scrolled-nav': scrollNav }">
    <nav>
      <div class="branding">
        <img src="/logo.png" alt="">
      </div>
      <ul class="navigation">
        <li>
          <router-link class="link" :to="{ name: '' }">Home</router-link>
        </li>
        <li>
          <router-link class="link" :to="{ name: '' }">About me</router-link>
        </li>
        <li>
          <router-link class="link" :to="{ name: '' }">Projects</router-link>
        </li>
        <li>
          <router-link class="link" :to="{ name: '' }">Contact me</router-link>
        </li>
      </ul>
      <div class="icon" @click="toggleMobileNav" v-show="mobile">
        <div class="hamburger">
          <span class=" bar" :class="{ 'icon-active': mobileNav }"></span>
          <span class="bar" :class="{ 'icon-active': mobileNav }"></span>
          <span class="bar" :class="{ 'icon-active': mobileNav }"></span>
        </div>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li>
            <router-link class="link" :to="{ name: '' }">Home</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">About me</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">Projects</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: '' }">Contact me</router-link>
          </li>
        </ul>
      </transition>
    </nav>
  </header>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const scrollNav = ref(false)
const mobileNav = ref(false)
const windowWidth = ref(Number)
const mobile = ref(Boolean)

const toggleMobileNav = () => {
  mobileNav.value = !mobileNav.value
}

onMounted(() => {
  window.addEventListener('resize', checkScreen)
  checkScreen
})

onMounted(() => {
  window.addEventListener('scroll', updatedScroll)
  updatedScroll
})

const updatedScroll = () => {
  const scrollPosition = window.scrollY
  if (scrollPosition > 500) {
    scrollNav.value = true
    return
  }
  scrollNav.value = false
}


const checkScreen = () => {
  windowWidth.value = window.innerWidth
  if (windowWidth.value <= 800) {
    mobile.value = true
    return
  }
  mobile.value = false
  mobileNav.value = false
  return
}
</script>

<style scoped>
header {
  background: rgba(0, 0, 0, .8);
  width: 100%;
  position: fixed;
  transition: 0.5s ease all;
  color: #fff;
  padding-block: 1em;
  z-index: 2;
  transition: 0.5s ease all;
}

header nav {
  position: relative;
  display: flex;
  flex-direction: row;
  padding: 12px 0;
  transition: 0.5 ease all;
  width: 90%;
  margin: 0 auto;
}

@media (min-width: 1140px) {
  header nav {
    max-width: 1140px;
  }
}

header nav ul,
header nav .link {
  font-weight: 500;
  color: #42b883;
  list-style: none;
  text-decoration: none;
}

header nav li {
  text-transform: uppercase;
  padding: 16px;
  margin-left: 16px;
}

.link {
  font-size: 14px;
  transition: 0.5s ease all;
  padding-bottom: 4px;
  border-bottom: 1px solid transparent;
}

.link:hover {
  border-color: #42b883;
}

.branding {
  display: flex;
  align-items: center;
}

.branding img {
  width: 50px;
  height: 50px;
  transition: 0.5s ease all;
}

.navigation {
  display: flex;
  align-items: center;
  flex: 1;
  justify-content: flex-end;
}

.icon {
  display: flex;
  align-items: center;
  position: absolute;
  top: 0;
  right: 24px;
  height: 100%;
}

.icon-active {
  transform: rotate(180deg);
}

.hamburger {
  display: none;
  cursor: pointer;
}

.bar {
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  -webkit-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
  background: #42b883;
  border-radius: 3px;
}

.dropdown-active {
  display: flex;
  flex-direction: column;
  position: fixed;
  width: 100%;
  max-width: 250px;
  height: 100%;
  background-color: #fff;
  top: 0;
  left: 0;
}

.dropdown-active li {
  margin-left: 0;
}

.dropdown-active li .link {
  color: #000;
}

.scrolled-nav {
  background-color: #000;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
}

.scrolled-nav nav {
  padding: 0;
}

.scrolled-nav nav .branding img {
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
}

@media (max-width: 800px) {
  .navigation {
    display: none;
  }

  .hamburger {
    display: block;
  }
}
</style>