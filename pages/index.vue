<template>
  <div>
    <b-navbar toggleable type="dark" variant="dark">
      <b-navbar-brand href="#">Rick and Morty</b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
          <b-icon v-else icon="chevron-bar-down"></b-icon>
        </template>
      </b-navbar-toggle>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="/">Link 1</b-nav-item>
          <b-nav-item href="/">Link 2</b-nav-item>
          <b-nav-item href="/" disabled>Disabled</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <b-container>
      <b-row>
        <b-col cols="12">
          <h1 class="text-center py-5 title">Rick and Morty</h1>
        </b-col>
        <b-col
          v-for="personaje in personajes"
          :key="personaje.id"
          cols="12"
          md="4"
        >
          <b-card-group class="mt-3 px-3" style="max-width: 400px">
            <b-card
              :title="personaje.nombre"
              :img-src="personaje.imagen"
              :img-alt="personaje.nombre"
              img-top
            >
              <b-card-text>
                <h4>Status: {{ personaje.status }}</h4>
              </b-card-text>
              <b-card-text>
                <h4>Especie: {{ personaje.especie }}</h4>
              </b-card-text>
            </b-card>
          </b-card-group>
        </b-col>
      </b-row>
    </b-container>
    <b-footer class="footer">
      <h3 class="text">2019</h3>
    </b-footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      personajes: [
        {
          id: 1,
          nombre: 'Morty',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 2,
          nombre: 'Rick',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 3,
          nombre: 'Summer',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 4,
          nombre: 'Beth',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 5,
          nombre: 'Jerry',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 6,
          nombre: 'Abadango',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/6.jpeg',
          status: 'Alive',
          especie: 'Animal',
        },
        {
          id: 7,
          nombre: 'Abradolf',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/7.jpeg',
          status: 'Alive',
          especie: 'Human',
        },
        {
          id: 8,
          nombre: 'Adjudicator',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/8.jpeg',
          status: 'unknown',
          especie: 'Human',
        },
        {
          id: 9,
          nombre: 'Agency',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/9.jpeg',
          status: 'Dead',
          especie: 'Human',
        },
      ],
    }
  },
}
</script>
<style>
body {
  background: rgb(43, 42, 42);
}
.card-body {
  background: rgb(70, 69, 69);
  color: white;
}
.title {
  color: aliceblue;
}

.text {
  font-size: 15px;
  padding: 30px 30px;
  color: aliceblue;
  background-color: rgb(51, 54, 54);
  height: 50px;
  margin-top: 50px;
}
</style>
