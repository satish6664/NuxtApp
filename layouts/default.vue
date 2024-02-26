<template>
    <div class="bg-indigo-200 text-gray-900 py-4">
      <div class="container mx-auto flex justify-between items-center">
        <!-- Left Side (Home) -->
        <div class="text-lg font-bold hover:text-white">
          <NuxtLink to="/" class="mr-4">Home</NuxtLink>
          <NuxtLink to="/Movies">Movies</NuxtLink>
        </div>
        
        <!-- Right Side (SignIn and Login) -->
        <div class="flex items-center">
          <NuxtLink to="/SignUp" class="text-lg font-bold text-gray-900 mr-4 hover:text-white">SignUp</NuxtLink>
          <NuxtLink to="/LogIn" class="text-lg font-bold text-gray-900 hover:text-white">Login</NuxtLink>
        </div>
      </div>
      <slot></slot>
    </div>
  </template>
  