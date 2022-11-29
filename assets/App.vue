<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Logo from '@/components/icons/IconLogo.vue'
</script>

<template>
  <nav>
    <RouterLink to="/">Projets</RouterLink>
    <Logo />
    <RouterLink to="/about">Contact</RouterLink>
  </nav>

  <RouterView />
</template>

<style>
@import '@/base.css';

#app{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

nav{
  width: 100%;
  height: 18rem;
  text-transform: uppercase;
  letter-spacing: .5rem;
  display: flex;
  justify-content: center;
  align-content: center;
}

nav a{
  color: var(--color-text);
  text-decoration: none;
  margin: auto 3rem;
  font-weight: 700;
}

nav a.router-link-exact-active {
  /* color: var(--color-text); */
  color: #FFA200;
}

dialog > *:not(p){
  width: 100%;
  height: 100%;
  max-width: 50vw;
  max-height: 50vh;
  object-fit: contain;
  /* border: none; */
  outline: none;
}
dialog > p{
  position: absolute;
  bottom: -40px;
  left: 50%;
  transform: translateX(-50%);
  color: #FFF;
  font-size: 18px;
  font-weight: 600;
  text-shadow: 0 0 2px #000;
}
</style>
