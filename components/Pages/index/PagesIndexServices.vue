<template>
		<section>
			<h3>Estamos aqui para ayudarte<br>descubre nuestros servicios</h3>
			<AppCard v-for="service in services" :key="service.title">
				<template v-slot:media>
					<figure class="card__image">
						<img :src="service.img" alt="imagen_card">
					</figure>
				</template>
				<h3>{{ service.title }}</h3>
				<p>{{ service.content }}</p>
				<NuxtLink class="buttom" :to="service.path" >Ver mas </NuxtLink>
			</AppCard>
		</section>
</template>
<script setup>
const services = [
	{
		img:"./assets/img/services-finance.jpg",
		title: "Finanzas",
		content: "El rol de las finanzas es la clave para la alta gerencia y para la toma de decisiones en general",
		path: "/servicios/finanzas"
	},
	{
		img:"./assets/img/services-development.jpg",
		title: "Desarrollo Organizativo ",
		content: "El cambio no es un fin, sino un medio para enfrentar la competencia.",
		path: "/servicios/desarrollo"
	},
	{
		img:"./assets/img/services-client.jpg",
		title: "Servicio al Cliente",
		content: "Ayudamos a las empresas a evaluar la calidad del servicio que estan brindando a sus clientes.",
		path: "/servicios/clientes"
	},
	{
		img:"./assets/img/services-recruitment.jpg",
		title: "Busqueda de personal ejecutivo",
		content: "Apoyamos a las empresas a encontrar al personal ideoneo para los puestos que necesita llenar",
		path: "/servicios/reclutamiento"
	},
	{
		img:"./assets/img/services-mentoring.jpg",
		title: "Gestion Humana",
		content: "La gestion humana es una especialidad estrategica en el manejo de las empresas",
		path: "/servicios/gestion"
	},
  ]
</script>

<style>

</style>