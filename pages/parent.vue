<template>
  <div>
    <h1>I am the parent view</h1>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/parent/child">Child</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/parent/child2">Child 2</NuxtLink>
        </li>
      </ul>
    </nav>
    <NuxtChild />
    <v-bottom-navigation style="margin-top: 50px" v-model="value" :dark="false" >
      <v-btn value="recent" @click="test">
        <span>Recent</span>

        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn value="favorites">
        <span>Favorites</span>

        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn value="nearby">
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>

<script>
export default {
  data: () => ({
    value: 'recent',
  }),
  methods: {
    test() {
      console.log('test')
    },
  },
}
</script>


<style scoped>
ul {
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
}
li {
  margin: 0 0.5rem;
  padding: 0.25rem;
  font-size: 1rem;
}
</style>