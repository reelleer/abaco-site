<template>
  <nav class="navbar">
    <ul class="navbar__list">
      <li v-for="link in links" :key="link.path" class="navbar__list-item">
        <NuxtLink :to="link.path">
        {{ link.name }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>
<script setup>
const links = [
  { path: "/", name: "Inicio" },
  { path: "/about", name: "Nosotros" },
  { path: "/services", name: "Servicios" },
  { path: "/clients", name: "Clientes" },
  { path: "/contact", name: "Contacto" },
]
</script>
<style>
.navbar {
  background: var(--background-color);
  color: white;
  height: calc(100vh - 54px)
}

.navbar__list {
  font-family: Poppins, sans-serif;
  list-style: none;
  padding-left: 1rem;
  font-size: 1.5rem;
}

.navbar__list-item a {
  color: white;
  display: inline-block;
  font-size: 1.25rem;
  padding: 0.75rem 0 0.75rem 0;
}

.navbar__list-item .router-link-active {
  border-top: 0.25rem solid var(--background-color-emphasis);
}

@media only screen and (min-width: 768px) {
  .navbar__list {
    margin: 0;
    padding: 0;
  }

  .navbar__list-item {
    display: inline;
    padding: 0 0;
  }

  .navbar__list-item:nth-child(n+1):not(:last-child){
    padding-right: 1rem;
  }

  .navbar {
    height: auto;
  }
}
</style>
