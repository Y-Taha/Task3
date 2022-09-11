<template>
    <div class="container">
        <h1 class="count">{{ storeCounter.count }}</h1>
        <div class="button">
            <button @click="storeCounter.increaseCount">+</button>
            <button @click="storeCounter.decreaseCount">-</button>
        </div>
    </div>
  </template>
<script setup>
    import {useCounterStore} from '@/stores/counter'
    const storeCounter =useCounterStore()
</script>

  <style scoped>
    html,body{
        padding: 0px;
        margin: 0px;
    }
    .container{
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }.container h1{
        font-size: 3rem;
        padding-bottom: 2vw;
        color: #fff;
    }
    .button{
        justify-content: space-between;
        justify-items: center;
        align-items: center;
        width: 15vw;
        height: 5vh;
        display: flex;
        flex-direction: row;
    }.button button{
        height: 5vh;
        width: 6vw;
        font-size: 2rem;
    }
  </style>