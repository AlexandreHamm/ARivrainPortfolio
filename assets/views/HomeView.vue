<script setup>

</script>

<template>
    <section>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
        <article></article>
    </section>
</template>

<style scoped>

section{
  width: 70%;
  display: grid;
  grid-template-columns: 2, 1fr;
  grid-auto-rows: 350px;
  grid-auto-flow: dense;
  grid-gap: 2rem;
}
article{
  position: relative;
  background: #AAA;
  overflow: hidden;
}

article:nth-child(6n+1){
  grid-column: 2;
  grid-row: span 2;
}
article:nth-child(6n+4) {
  grid-column: 1;
  grid-row: span 2;
}

article::after{
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  background: #CD3341;
  opacity: 0;
  transition: .3s linear;
}
article:hover::after{
  width: calc(100% - 5rem);
  height: calc(100% - 5rem);
  opacity: .7;
  transition: .3s linear;
}
</style>
