<!-- <template>
    <div class="p-6 bg-gray-100">
      <h2 class="text-xl font-semibold mb-4">Sign Up</h2>
      <form @submit.prevent="signup" class="space-y-4">
        <input type="text" v-model="username" placeholder="Username" required class="border border-gray-300 rounded-md px-3 py-2 w-full">
        <input type="password" v-model="password" placeholder="Password" required class="border border-gray-300 rounded-md px-3 py-2 w-full">
        <input type="submit" value="Sign Up" class="bg-blue-500 text-white font-semibold rounded-md py-2 px-4 hover:bg-blue-600 cursor-pointer">
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref, getCurrentInstance } from 'vue';
  
  const instance = getCurrentInstance();
  const emit = instance.emit;
  
  const username = ref('');
  const password = ref('');
  
  const signup = (event) => {
    // Prevent form submission
    event.preventDefault();
    
    // Emit an event to send sign-up data to the parent component
    emit('signup', { username: username.value, password: password.value });
    // Clear the form fields after sign-up
    username.value = '';
    password.value = '';
    // Show alert
    window.alert('User signed up successfully!');
  };
  </script>
  
  <style>
  /* Add any custom styles here */
  </style>
   -->



   <template>
    <div>page 2</div>
   </template>