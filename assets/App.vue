<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Logo from '@/components/icons/IconLogo.vue'
</script>

<template>
  <nav>
    <RouterLink to="/">Projects</RouterLink>
    <Logo />
    <RouterLink to="/about">About me</RouterLink>
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
  height: 10rem;
  margin-bottom: 5rem;
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
}

nav a.router-link-exact-active {
  /* color: var(--color-text); */
  color: #CD3341;
}
</style>
