<template>
  <div class="flex flex-row">
    <Toolbar @onClickToolbarBtn="toggleSidebar" />
    <expandable :expandable_type="expandable_type"  v-show="collapse_sidebar" />
    <div class="flex flex-col">
      <button
      @click="collapse_sidebar = !collapse_sidebar"
        style="position: absolute;
    top: 50%;"
        class="rounded bg-gray"
      >
        <i :class="`fa ${ collapse_sidebar === true ?  'fa-arrow-left' : 'fa-arrow-right' }`"></i>
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

  data(){
    return{
      collapse_sidebar: false,
      expandable_type: ""
    }
  },
  methods:{
    toggleSidebar(expandable_type){
      this.collapse_sidebar = !this.collapse_sidebar
      this.expandable_type = expandable_type
    }
  }
};
</script>

<style lang="scss" scoped></style>
