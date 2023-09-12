<template>
  <div id="my-header">
    <header>
      <NuxtLink to="/">Nuxt logo</NuxtLink>
      <nav>
        <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
      </nav>
    </header>
  </div>

  <!-- Output other component page -->
  <div>
    <slot />
  </div>
</template>

<style scoped>
#my-header {
  background-color: #333; /* Background color for the header */
  color: #fff; /* Text color for the header */
  padding: 20px; /* Add padding to the header */
  display: flex;
  justify-content: space-between; /* Align logo and navigation horizontally */
  align-items: center; /* Center align items vertically */
}

#my-header a {
  color: #fff; /* Text color for the header links */
  text-decoration: none; /* Remove underlines from links */
  margin: 0 10px; /* Add margin to separate links */
  display: inline-block; /* Make links inline-block to control spacing */
}

#my-header ul {
  list-style: none; /* Remove list bullets */
  padding: 0; /* Remove default padding for ul */
  display: flex; /* Use flex layout for the list items */
}

#my-header li {
  margin: 0; /* Remove default margin for list items */
}

/* You can add more styles for navigation, logo, etc. */
</style>
