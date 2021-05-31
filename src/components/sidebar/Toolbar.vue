<template>
  <div id="toolbar">
    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-columns"></i>
        <span>
          Template
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-image"></i>
        <span>
          Photos
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-shapes"></i>
        <span>
          Elements
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-font"></i>
        <span>
          Texts
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-music"></i>
        <span>
          Audio
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-video"></i>
        <span>
          Video
        </span>
      </button>
    </div>

    <div class="">
      <button class="toolbar-items" style="width: 100%">
        <i class="fas fa-chalkboard"></i>
        <span>
          Background
        </span>
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#toolbar {
  display: flex;
  flex-direction: column;
  background: #222;
  color: #bbb;
  font-size: 12px;
  font-family: Verdana, "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, sans-serif;
}

.toolbar-items {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 17px 25px;
}

.toolbar-items > svg {
  font-size: 25px;
  margin-bottom: 5px;
  color: #bbb;
}
</style>
