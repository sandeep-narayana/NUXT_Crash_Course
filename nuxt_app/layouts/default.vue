<template>
  <div>
    <header class="shadow-sm bg-white">
      <NuxtLink to="/" class="font-bold">Nuxt logo</NuxtLink>
      <nav class="container mx-auto p-4 flex justify-between">
        <ul class="flex gap-4">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
      </nav>
    </header>
  </div>

  <!-- Output other component page -->
  <div class="container mx-auto p-4">
    <slot />
  </div>
</template>
