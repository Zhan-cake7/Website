<template>
    <header class= "flex flex-row w-full bg-[#DBD8D0] p-4">
      <div class= "basis-1/4 flex items-center justify-start">
        <img src= "assets/images/Roblox.png" class="w-16 h-16">
      </div>
      <div class = "basis-1/4">
      </div>
      <nav class="basis-1/2 flex flex-row items-center justify-end px-4 gap-4">
        <NuxtLink to="/" class="my-auto p-2 hover:bg-gray-500 hover:text-white">Home</NuxtLink>
        <NuxtLink to="/Lab3" class="my-auto p-2 hover:bg-gray-500 hover:text-white">Lab3</NuxtLink>
        <NuxtLink to="#" class="my-auto p-2 hover:bg-gray-500 hover:text-white">LogIn</NuxtLink>
        <NuxtLink to="#" class="my-auto p-2 hover:bg-gray-500 hover:text-white">LogOut</NuxtLink>
      </nav>
    </header>
  
    <main class = 'p-5 flex bg-[#DDDEE5] h-screen'>
    <slot />
  </main>

    <footer class = "flex flex-row w-full bg-[#DBD8D0] border-t-2 border-gray-400 items-center justify-center px-4 py-2 gap-4">
    <a href = "https://www.youtube.com/"><img src = "assets/images/youtube.png" claass = "w-16 h-16"></img></a>
    <a href = "https://github.com/"><img src = "assets/images/github.png" claass = "w-16 h-16"></img></a>
    <a href = "https://www.facebook.com/"><img src = "assets/images/facebook.png" claass = "w-16 h-16 bg-transparent"></img></a>
  </footer>
    </template>
   
   <script setup lang="ts">
    import { useHead } from '#app';
    import {ref} from 'vue'
    
    useHead({
        script: [
            {
                async: true,
                src: "https://www.googletagmanager.com/gtag/js?id=G-0PX1T3FNCZ"
            },
            {
                innerHTML:`window.dataLayer = window.dataLayer || [];
                function gtag(){dataLayer.push(arguments);}
                gtag('js', new Date());
                gtag('config', 'G-0PX1T3FNCZ')
            `,
                type: 'text/javascript',
            },
        ],
        __dangerouslyDisableSanitizerByTagID: {
            gtag: ['innerHTML'],
        },
    });
    </script>