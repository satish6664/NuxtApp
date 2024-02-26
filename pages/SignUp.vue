<template>
    <div class="flex justify-center items-center h-screen bg-gray-100">
      <div class="p-8 bg-white shadow-lg rounded-lg">
        <h2 class="text-3xl font-bold mb-4 text-center text-gray-800">Sign Up</h2>
        <form @submit.prevent="signup" class="space-y-4">
          <div class="relative">
            <input type="text" v-model="username" placeholder="Username" required class="border border-gray-300 rounded-md px-3 py-2 w-full focus:outline-none focus:border-blue-500">
            <div class="absolute inset-y-0 right-0 flex items-center pr-3">
              <svg class="h-6 w-6 text-gray-400" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor">
                <path d="M17 21l4-4m0 0l-4-4m4 4H3"></path>
              </svg>
            </div>
          </div>
          <div class="relative">
            <input type="password" v-model="password" placeholder="Password" required class="border border-gray-300 rounded-md px-3 py-2 w-full focus:outline-none focus:border-blue-500">
            <div class="absolute inset-y-0 right-0 flex items-center pr-3">
              <svg class="h-6 w-6 text-gray-400" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor">
                <path d="M17 21l4-4m0 0l-4-4m4 4H3"></path>
              </svg>
            </div>
          </div>
          <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 transition duration-300 ease-in-out w-full">Sign Up</button>
        </form>
      </div>
    </div>
  </template>
  
  
  
  <script setup>
  const signupData=usersList()
  
  const username = ref('');
  const password = ref('');
  
  const signup = (event) => {
    event.preventDefault();
    
    signupData.value.push({user:username.value,pass:password.value})
    console.log(signupData.value);

    username.value = '';
    password.value = '';
    // window.alert('User signed up successfully!');
    navigateTo('/LogIn');
  };
  useHead({
    title:"SignUp Page"
  })
  </script>
  
  <style>
  /* Add any custom styles here */
  </style>
  