<template>
  <div
    ref="expandable_container"
    style="background: #222;"
    class="overflow-y-auto"
  >
    <search-template style="max-width: 300px; width: 100%" />

    <div
      v-for="category in categories"
      :key="category"
      class="m-4"
      style="max-width: 300px; width: 90%;"
    >
      <div class="flex flex-row mb-3">
        <span class="flex-grow text-white">{{ category }} </span>
        <span class="text-gray-500"> view all</span>
      </div>

      <div class="flex flex-row overflow-x-auto">
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
        <img
          @dragstart="drag"
          src="/templates/canva_template.png"
          alt="template"
          width="100px"
          class="px-2 mb-3"
        />
      </div>
    </div>
  </div>
</template>

<script>
import SearchTemplate from "./SearchTemplate";
export default {
  components: { SearchTemplate },
  mounted() {
    this.$refs.expandable_container.height = window.innerHeight;
    console.log(this.$refs.expandable_container.height);
  },
  data() {
    return {
      categories: ["recent", "covid", "wishes", "sorry"],
    };
  },
  methods: {
    drag(ev) {
      ev.dataTransfer.setData("text", ev.target.id);
    },
  },
};
</script>

<style lang="scss" scoped></style>
