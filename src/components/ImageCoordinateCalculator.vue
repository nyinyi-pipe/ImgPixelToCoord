<!-- <template>
  <div>
    <canvas ref="canvas" @click="calculateCoordinates"></canvas>
  </div>
</template>


<script>
export default {
  mounted() {
    this.canvas = this.$refs.canvas;
    this.context = this.canvas.getContext('2d');
    this.image = new Image();
    this.image.src = ''; // Replace with your image path
    this.image.onload = this.drawImage;
  },
  methods: {
    drawImage() {
      this.canvas.width = this.image.width;
      this.canvas.height = this.image.height;
      this.context.drawImage(this.image, 0, 0);
    },
    calculateCoordinates(event) {
      const rect = this.canvas.getBoundingClientRect();
      const x = event.clientX - rect.left;
      const y = event.clientY - rect.top;
      console.log(`Clicked coordinates: (${x}, ${y})`);
    },
  },
};
</script> -->



<template>
  <div>
    <canvas ref="canvas" @click="calculateCoordinates"></canvas>
  </div>
</template>

<script>
export default {
  mounted() {
    this.canvas = this.$refs.canvas;
    this.context = this.canvas.getContext('2d');
    this.image = new Image();    
    this.image.src = '1/1.png'; // Replace with the actual path to your image file
    this.image.onload = this.drawImage;
  },
  methods: {
    drawImage() {
      this.canvas.width = this.image.width;
      this.canvas.height = this.image.height;
      this.context.drawImage(this.image, 0, 0);
    },
    calculateCoordinates(event) {
      const rect = this.canvas.getBoundingClientRect();
      const x = event.clientX - rect.left;
      const y = event.clientY - rect.top;
      console.log(`Clicked coordinates: (${x}, ${y})`);
    },
  },
};
</script>

<style scoped>
canvas {
  border: 1px solid #000;
}
</style>
