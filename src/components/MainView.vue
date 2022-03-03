<template>
  <form>
    <div v-for="res in response" :key="res.data[0].woeid">
      <h1 class="title">{{ res.data[0].title }}</h1>
      <p>{{ res.data[0].location_type }}</p>
      <p>Coordinates: {{ res.data[0].latt_long }}</p>
    </div>
  </form>
</template>

<script>
export default {
  props: ["response"],
};
</script>

<style>
</style>