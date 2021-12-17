<template>
  <div>
    <fetch-data
      v-slot="{ response, loading }"
      url="https://jsonplaceholder.typicode.com/users/1"
    >
      <!-- ... response, loading 을 가져올수 있다-->
      <div>
        <div v-if="!loading">
          <p v-for="el of Object.entries(response)">
            {{el[0]}} : {{el[1]}}
          </p>
          <!-- <p>{{ response.name }}</p>
          <p>{{ response.email }}</p> -->
        </div>
        <div v-if="loading">
          loading...
        </div>
      </div>
    </fetch-data>
  </div>
</template>

<script>
import FetchData from "./components/FetchData.vue";

export default {
  components: {
    FetchData,
  },
};
</script>
