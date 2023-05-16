<script setup>
import { onMounted } from 'vue'
import Granim from 'granim';
onMounted(()=>{
  init()
})
const init = () => {
  let granimInstance = new Granim({
    element: '#canvas-complex',
    direction: 'custom',
    customDirection: {
      x0: '40%',
      y0: '10px',
      x1: '60%',
      y1: '50%',
    },
    isPausedWhenNotInView: true,
    states : {
      "default-state": {
        gradients: [
          [
            { color: '#833ab4', pos: .2 },
            { color: '#fd1d1d', pos: .8 },
            { color: '#38ef7d', pos: 1 }
          ], [
            { color: '#40e0d0', pos: 0 },
            { color: '#ff8c00', pos: .2 },
            { color: '#ff0080', pos: .75 }
          ],
        ]
      }
    }
  });
}
</script>

<template>
  <canvas id="canvas-complex" style="width: 100%; height:400px"></canvas>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
