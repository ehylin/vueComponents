<template>
  <div class="hello">
    <ul id="personajes">
      <li
        class="personaje"
        v-for="(personaje, $index) in personajes"
        :key="$index"
      >
        <img class="personaje-img" :src="personaje.src" alt="" />
        {{ personaje.nombre }}
      </li>
    </ul>

    <!-- <div
      class="div-personajes"
      v-for="(personaje, $index) in personajes"
      :key="$index"
    >
      <img class="personaje-img" :src="personaje.src" alt="" />
      <p class="personaje">{{ personaje.nombre }}</p>
    </div> -->
    <!-- <ul v-for="(personaje, $index) in personajes" :key="$index">
      <li>{{ $index }}</li>
      <li>{{ personaje.nombre }}</li>
      <li>{{ personaje.src }}</li>
    </ul> -->
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    personajes: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#personajes {
  padding: 0;
}
.personaje {
  color: green;
  list-style-type: none;
  position: relative;
  display: flex;
  padding: 0.5rem 1rem;
  align-items: center;
}
.personaje-img {
  border-radius: 50%;
  width: 90px;
}
</style>
