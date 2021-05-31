<template>
  <div class="flex flex-row">
    <Toolbar />
    <expandable />
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
