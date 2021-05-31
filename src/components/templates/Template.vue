<template>
  <div class="flex flex-col">
    <div class="flex flex-row ">
      <div class="flex-1">
        <span>
          Page 1 - Add Title
        </span>
      </div>

      <div class="flex flex-row mx-4">
        <span class="mx-2">
          <i class="fas fa-chevron-up"></i>
        </span>

        <span class="mx-2">
          <i class="fas fa-chevron-down"></i>
        </span>

        <span class="mx-2">
          <i class="fas fa-clone"></i>
        </span>

        <span class="mx-2">
          <i class="fas fa-plus-square"></i>
        </span>

        <span class="mx-2">
          <i class="fas fa-trash-alt"></i>
        </span>
      </div>
    </div>

    <div class="border border-0 mt-3" style="height : 500px" >
      <canvas height="500px" width="600px" ref="template"></canvas>
    </div>
  </div>
</template>

<script>
import {fabric} from 'fabric'

export default {
  mounted(){
      const ref = this.$refs.template;
      const canvas = new fabric.Canvas(ref);
      const rect = new fabric.Rect({
        fill: 'red',
        width: 20,
        height: 20
      });
      canvas.add(rect);
  }
};
</script>

<style lang="scss" scoped></style>
