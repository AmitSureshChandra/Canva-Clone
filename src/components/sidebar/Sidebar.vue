<template>
  <div class="flex flex-row">
    <Toolbar />
    <expandable />
    <div class="flex flex-col">
      <button
        style="position: absolute;
    top: 50%;"
        class="rounded bg-gray"
      >
        <i class="fa fa-arrow-left"></i>
      </button>
    </div>
  </div>
</template>

<script>
import Expandable from "./Expandable";
import Toolbar from "./Toolbar";

export default {
  components: {
    Toolbar,
    Expandable,
  },
};
</script>

<style lang="scss" scoped></style>
