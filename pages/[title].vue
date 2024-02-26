<template>
    <div class="flex items-center justify-center h-screen">
      <div class="max-w-lg w-full bg-white shadow-md rounded-lg overflow-hidden flex">
        <!-- Left side with enlarged image -->
        <div class="w-1/2">
          <img :src="`/images/${name}.jpg`" class="w-full h-auto transition-transform duration-300 transform hover:scale-110" alt="Movie Poster">
        </div>
        
        <!-- Right side with highlighted text contents -->
        <div class="w-1/2 p-4 bg-gray-100">
          <div class="text-lg font-semibold mb-2 text-blue-600">{{ name }}</div>
          <div class="text-sm mb-4 text-gray-800">
            <h1>RamCharan | Jr.NTR | Alia </h1>
            <p class="mb-2">Rating : 8.9</p>
            <p class="mb-2">RRR is an Indian film that tells the fictional story of two freedom fighters who fought against the British Raj and the Nizam of Hyderabad in the 1920s.</p>
          </div>
          <!-- Wishlist button -->
          <button class="bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 transition duration-300 ease-in-out">Add to Watchlist</button>
        </div>
      </div>
    </div>
  </template>
  
  
  
<script setup>

const route=useRoute()
const name=computed(()=>{
    return `${route.params.title}`
})
console.log(name.value)
</script>
<style>
img{
    width: 250px;
}
</style>