<!-- <template>
    <div class="p-6 bg-gray-100">
      <h2 class="text-xl font-semibold mb-4">Login</h2>
      <form @submit.prevent="login" class="space-y-4">
        <input type="text" v-model="username" placeholder="Username" required class="border border-gray-300 rounded-md px-3 py-2 w-full">
        <input type="password" v-model="password" placeholder="Password" required class="border border-gray-300 rounded-md px-3 py-2 w-full">
        <input type="submit" value="Login" class="bg-blue-500 text-white font-semibold rounded-md py-2 px-4 hover:bg-blue-600 cursor-pointer">
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { defineProps } from 'vue'; // Import defineProps
  
  // Define props
  const props = defineProps({
    signupData: {
      type: Object,
      default: null
    }
  });
  
  // Define reactive variables
  const username = ref('');
  const password = ref('');
  
  // Method to handle login
  const login = () => {
    // Check if signupData is null
    if (!props.signupData) {
      window.alert('No sign-up data available.');
      return;
    }
  
    // Get sign-up data from props
    const { username: signupUsername, password: signupPassword } = props.signupData;
  
    // Check if login credentials match sign-up data
    if (username.value === signupUsername && password.value === signupPassword) {
      window.alert('User logged in successfully!');
    } else {
      window.alert('Invalid username or password');
    }
  };
  </script>
   -->

   <template>
    <div>page 1</div>
   </template>