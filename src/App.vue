<template>
  <div>
    <NavBar :query="query" :handleSearch="handleSearch" />
    <MainView :response="handleSearch(response)" />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import MainView from "./components/MainView.vue";
import axios from "axios";
import { ref } from "@vue/reactivity";

export default {
  components: { NavBar, MainView },
  setup() {
    const query = ref("");

    const handleSearch = (response) => {
      axios
        .get(
          `https://www.metaweather.com/api/location/search/?query=${query.value}`
        )
        .then((res) => {
          const response = res.data;
          console.log(response.data);
        });
      return response;
    };

    return { query, handleSearch };
  },
};
</script>

<style>
</style>
