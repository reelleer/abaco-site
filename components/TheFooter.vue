<template>
  <footer class="footer">
    <div class="container">
      <div class="text-white">
        <p>
        Sobre <b class="text-emphasis">ABACO</b>.
        </p>
        <p>
        Somos un equipo de profesionales que promovemos una cultura de
        efectividad en empresas y queremos apoyarlos.
        </p>
        <ul class="list-icon">
          <li>
            <AppIcon name="geo-alt" /> Edificio Kakau, Camino de oriente piso 8
            Modulo A-801
          </li>
          <li>
            <AppIcon name="telephone" /> 
            <a class="text-white" href="tel:+50588102929">+505 8810-2929</a>
          </li>
          <li>
            <AppIcon name="envelope" /> 
            <a class="text-white" href="mailto:abaco@abaco.com.ni">
              abaco@abaco.com.ni
            </a>
          </li>
        </ul>
      </div>
      <div class="footer__logo">
        <AppLogo color="white" />
      </div>
    </div>
  </footer>
</template>
<style>
.footer {
  background-color: var(--background-color-alternate);
}

.footer__logo {
  text-align: center;
}

@media only screen and (min-width: 768px) {
  .footer .container {
    display: flex;
    gap: 1rem;
    justify-content: space-between;
  }

  .footer__logo {
    align-self: center;
  }
}
</style>

