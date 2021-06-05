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

    <div class="border border-0 mt-3" style="height : 500px">
      <div @drop="drop" @dragover="allowDrop">
        <canvas ref="template"></canvas>
      </div>
    </div>
  </div>
</template>

<script>
import { fabric } from "fabric";

export default {
  data() {
    return {
      canvas: null,
      clientX: 0,
      clientY: 0,
    };
  },
  mounted() {
    const ref = this.$refs.template;
    this.canvas = new fabric.Canvas(ref);
    const rect = new fabric.Rect({
      fill: "red",
      width: 20,
      height: 20,
    });
    this.canvas.add(rect);
  },
  methods: {
    drop(ev) {
      ev.preventDefault();
      var data = ev.dataTransfer.getData("text");

      let canvasBox = this.$refs.template.getBoundingClientRect();

      var pugImg = new Image();
      pugImg.onload = () => {
        let left = this.clientX - canvasBox.x;
        let top = this.clientY - canvasBox.y;
        let width = pugImg.width ?? 300;
        let height = pugImg.height ?? 300;

        var pug = new fabric.Image(pugImg, {
          // angle: 45,
          width,
          height,
          left,
          top,
          scaleX: 0.25,
          scaleY: 0.25,
        });
        this.canvas.add(pug);
      };
      pugImg.src = data;
    },

    allowDrop(ev) {
      ev.preventDefault();
      this.clientX = ev.clientX;
      this.clientY = ev.clientY;

      console.log({ clientX: this.clientX });
      console.log({ clientY: this.clientY });
    },
  },
};
</script>

<style lang="scss" scoped></style>
