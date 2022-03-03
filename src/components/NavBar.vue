<!-- This is the navbar component -->

<template>
  <nav class="navbar navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand">Navbar</a>
      <form class="d-flex">
        <input
          class="form-control me-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
          v-model="query"
        />
        <button
          class="btn btn-outline-success"
          type="submit"
          @click.prevent="handleSearch"
        >
          Search
        </button>
      </form>
    </div>
  </nav>
</template>

<script>
export default {
  props: ["query", "handleSearch"],
};
</script>

<style>
</style>