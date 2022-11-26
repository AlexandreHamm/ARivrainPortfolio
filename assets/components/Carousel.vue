<script setup>

</script>

<template>
    <section>
        <div>
            <img src="@/img/fia/1.jpg" alt="">
            <img src="@/img/fia/2.jpg" alt="">
            <img src="@/img/fia/3.jpg" alt="">
            <img src="@/img/fia/4.jpg" alt="">
            <img src="@/img/fia/5.jpg" alt="">
            <img src="@/img/fia/6.jpg" alt="">
            <img src="@/img/fia/7.jpg" alt="">
            <img src="@/img/fia/8.jpg" alt="">
            <img src="@/img/fia/9.jpg" alt="">
        </div>
    </section>
</template>

<style scoped>
    section{
        width: 100%;
        height: 70vh;
    }
    div{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 600px !important;
        overflow: hidden;
    }
    div img{
        position: absolute;
        right: -100vw;
        transform: translateX(50%);
        width: auto;
        height: 100%;
        object-fit: contain;
        transition: right 2s, opacity .7s;
        opacity: 0;
    }
    div img:first-child{
        right: 50%;
        transform: translateX(50%);
        opacity: 1;
    }
    div:hover img:first-child{
        right: 100vw;
        transition: right 2s, opacity .7s;
        opacity: 0;
    }
    div:hover img:nth-child(2){
        right: 50%;
        transform: translateX(50%);
        transition: right 2s, opacity .7s;
        opacity: 1;
    }
</style>