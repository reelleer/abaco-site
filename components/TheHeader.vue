<template>
  <header class="header">
    <div class="container">
      <AppLogo color="light" />
      <ul class="header__menu">
        <li>Inicio</li>
        <li>Nosotros</li>
        <li>Servicios</li>
        <li>Clientes</li>
        <li>Contacto</li>
      </ul>
      <svg class="header__mobile-icon" xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
      </svg>
    </div>
  </header>
</template>
<style>
.header {
  background-color: var(--background-color);
  height: 3.375rem;
}

.header .container {
  --calc-padding-top-bottom: calc((54px - 32px) / 2);
  display: flex;
  justify-content: space-between;
  padding-bottom: var(--calc-padding-top-bottom);
  padding-top: var(--calc-padding-top-bottom);
}

.header__menu {
  display: none;
}

.header__menu--display {
  display: block;
  left: 0px;
  position: absolute;
  top: 55px;
}

.header__mobile-icon {
  color: white;
}
</style>
