<template>
  <div class="min-h-screen bg-cover bg-center flex justify-center items-center" style="background-image: url('https://hdqwalls.com/wallpapers/dunkirk-2017-movie-4k.jpg')">
    <div class="text-center">
      <h2 class="text-3xl font-bold mb-4 text-white hover:text-gray-200 transition duration-300 ease-in-out">Welcome to Our Website</h2>
      <router-link to="/signup" class="bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 transition duration-300 ease-in-out inline-block">Sign Up</router-link>
    </div>
  </div>
</template>
<script setup>

useHead({
  title:'Home Page'
})
</script>