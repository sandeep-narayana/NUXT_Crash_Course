<template>
  <div>
    <header class="shadow-sm bg-white">
      <NuxtLink to="/products" class="font-bold">Nuxt Dojo Merch</NuxtLink>
    </header>
  </div>

  <!-- Output other component page -->
  <div class="container mx-auto p-4">
    <slot />
  </div>

  <footer class="container mx-auto p-4 flex justify-between border-t-2">
    <ul class="flex gap-4">
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/about">About</NuxtLink></li>
      <li><NuxtLink to="/products">Products</NuxtLink></li>
    </ul>
  </footer>
</template>
