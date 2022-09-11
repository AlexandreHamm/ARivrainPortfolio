<script setup>

</script>

<template>
    <section>
        <div>Test</div>
        <div></div>
        <div></div>
    </section>
</template>

<style scoped>
section{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 20px;
    grid-row-gap: 20px;
}
div{
    background: #FFF;
    width: 200px;
    height: 100px;
}
</style>