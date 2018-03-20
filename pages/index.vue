<template>
  <section class="container">
    <div class="center">
      <h1 class="title">
        crossover<span>X</span>developer
      </h1>
      <a href="https://medium.com/@iddar/descubriendo-un-nuevo-camino-135202f816ca">HISTORY</a>
    </div>
  </section>
</template>

<script>
import ContactForm from '~/components/ContactForm.vue'

export default {
  components: {
    ContactForm
  },
  head: {
    link: [
      { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Arizonia|Mina:400,700' }
    ]
  }
}
</script>

<style>
body {
  background: url('~/assets/background.jpeg') center top;
  color: #ffffff;
  font-family: 'Mina', sans-serif;
  height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;
}

.center {
  text-align: center;
}

.title {
  font-size: 2.5rem;
  color: #e0d5d8ad;
  cursor: default;
  transition: color ease .3s;
}

.title:hover {
  color: #fff;
}

.title span {
  font-size: 4em;
  font-weight: 700;
  vertical-align: middle;
  font-family: Arizonia;
  margin-right: -15px;
  margin-left: -5px;
}

a {
  color: #fff;
}

</style>
