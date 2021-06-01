<template>
  <div class="pt-5">
    <div
      class="m-4 pr-1 mt-0 bg-white px-3 search-container  rounded flex flex-row"
    >
      <i class="fa fa-search mt-3" />
      <input
        class="m-2 "
        type="text"
        name="search"
        id="search"
        placeholder="Search"
      />

      <i class="fa fa-filter mt-1 text-3xl border border-1 p-1" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchTemplate",
};
</script>

<style scoped>
.search-container {
  height: 40px;
}
</style>
