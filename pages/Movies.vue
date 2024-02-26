<template>
    <div class="container mx-auto px-4 py-8" :class="{ 'dark': darkMode }">
      <div class="flex flex-col">
        <div class="flex items-center justify-between mb-4">
          <input type="text" v-model="search" placeholder="Search Movie" @input="filterMovies" class="flex-grow px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:border-indigo-500 focus:ring focus:ring-indigo-200">
          <button @click="toggleDarkMode" class="ml-4 bg-gray-200 dark:bg-gray-800 text-gray-800 dark:text-gray-200 px-4 py-2 rounded-md shadow-md transition-colors duration-300">Theme</button>
        </div>
        <div class="SearchList">
          <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
            <div v-for="movie in filteredMovies" :key="movie.id" class="max-w-xs mx-auto overflow-hidden rounded-lg shadow-lg hover:shadow-xl transition duration-300 ease-in-out">
              <nuxt-link :to="`/${movie.route}`" class="block">
                <div class="relative">
                  <img :src="`/images/${movie.image}`" :alt="movie.title" class="object-cover w-full h-96 transition duration-300 transform hover:scale-105">
                  <div class="absolute inset-0 flex items-center justify-center opacity-0 hover:opacity-100 transition duration-300 ease-in-out bg-black bg-opacity-50">
                    <span class="text-white text-lg font-semibold">View Details</span>
                  </div>
                </div>
                <div class="p-4">
                  <h1 :class="{ 'text-white': darkMode, 'text-gray-800': !darkMode }" class="text-xl font-semibold">{{ movie.title }}</h1>
                </div>
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  
  <script>
  import { ref, computed } from 'vue';
  
  export default {
    setup() {
      const search = ref('');
      const darkMode = ref(false); // Initially, light mode is enabled
  
      const movies = ref([
        { id: 1, route: 'OG', image: 'OG.jpg', title: 'OG' },
        { id: 2, route: 'Wakanda', image: 'Wakanda.jpg', title: 'Wakanda' },
        { id: 9, route: 'Saaho', image: 'Saaho.jpg', title: 'Saaho' },
        { id: 8, route: 'RRR',image:'RRR.jpg',title:'RRR'},
        { id: 3, route: 'Sicario', image: 'Sicario.jpg', title: 'Sicario' },
        { id: 4, route: 'Rangasthalam', image: 'Rangasthalam.jpg', title: 'Rangasthalam' },
        { id: 5, route: 'BladeRunner', image: 'BladeRunner.jpg', title: 'BladeRunner' },
        { id: 6, route: 'BlackPanter', image: 'BlackPanter.jpg', title: 'BlackPanter' },
        { id: 7, route: 'JohnWick', image: 'JohnWick.jpg', title: 'JohnWick' }
      ]);
  
      const filteredMovies = computed(() => {
        return movies.value.filter(movie =>
          movie.title.toLowerCase().includes(search.value.toLowerCase())
        );
      });
  
      const filterMovies = () => {
        // Implement filtering logic here
      };
  
      const toggleDarkMode = () => {
        darkMode.value = !darkMode.value; // Toggle dark mode
      };
  
      return { search, filteredMovies, filterMovies, darkMode, toggleDarkMode };
    }
  };
  </script>
  
  <style scoped>
  /* Add any custom styles here */
  .dark {
    background-color: #1a202c; /* Dark mode background color */
  }
  </style>
  