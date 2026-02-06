<script setup>
import { ref } from 'vue'
 const counter = ref(0)
 const increment = () => {
    counter.value++
 }
 const decrement = () => {
    counter.value-- 
 }
</script>


<template>

    <div class="counter-container"> 
       <h1>Counter: {{ counter }}</h1>
       <div class = "btn-container">
        <button @click="increment" > +</button>
        <button @click="decrement" :disabled="counter<=0">-</button>
        </div>
    </div>
</template>

<style scoped>
.counter-container{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 90vw;
    height: 100vh;
  }
h1{
    font-size: 40px;
    margin-bottom: 20px;
    color: blueviolet;
}
  .btn-container{
    display: flex;
    flex-direction: row;
    gap: 20px;
    margin-top: 20px;
    size: 60px;
    button{
        background-color: rgb(24, 3, 50);
        border: 2px solid #6b1250;
        border-radius: 20px;
        padding: 20px;
        width: 150px; 
        font-size: 20px;
        text-align: center;
        color: white;
        box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
  }
  :disabled{
    opacity: 0.5;
    cursor: not-allowed;
  }

  </style>
