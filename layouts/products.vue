<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/products">Nuxt Dojo Merche</NuxtLink>
      </nav>
    </header>
    <!-- output the page content -->
    <div><slot /></div>
  </div>

  <footer>
    <ul>
      <li>
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/products">Products</NuxtLink>
      </li>

      <a href="/about">noraml link -- about page</a>
    </ul>
  </footer>
</template>

<style scoped>
.router-link-exact-active {
  color: purple;
}
</style>
