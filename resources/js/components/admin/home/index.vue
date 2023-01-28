<script setup>
   import { useRouter } from "vue-router"
   
   const router = useRouter()

   const logout = () => {
    localStorage.removeItem('token')
    router.push('/') 
   }
</script>

<template>
    <h1>Welcome to admin overview </h1>

    <div>
       <router-link to="/">Home page</router-link> 
    </div>
    <br>
    <button @click="logout">
        Log out
    </button>
</template>