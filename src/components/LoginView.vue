<script setup lang="ts">
import {ref} from 'vue';
import axios from 'axios';

const email = ref<String>();
const password = ref<String>();



const login = () => {
    const obj = {
        email : email.value,
        password : password.value,
    }
   axios({
  method: 'post',
  url: 'https://zany-tan-cow-hose.cyclic.app/api/auth/login',
  data: {
    email: 'test2@test.com',
    password: 'password'
  }
});
    
}



</script>
<template>

<div>
    <form action="" @submit.prevent="login()">
         <div class="email-block">
        <label for="email">Email</label>
        <input type="text" v-model="email" id="email">
    </div>
   
    <div class="password-block">
        <label for="password">Password</label>
        <input type="text" v-model="password" id="password">
    </div>
        <div class="email-block">
        <button>submit</button>
    </div>
    </form>
   
</div>
    
</template>