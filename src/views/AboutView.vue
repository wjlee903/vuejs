<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1 v-for="num in 3" :key="num">{{num}}</h1>
  </div>
</template>
