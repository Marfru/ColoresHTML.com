<template>
  <div :style="{ background: color }">
    <color-picker
      theme="light"
      :color="color"
      :sucker-hide="true"
      :sucker-canvas="suckerCanvas"
      :sucker-area="suckerArea"
      @changeColor="changeColor"
      @openSucker="openSucker"
    />
  </div>
</template>

<script>
import colorPicker from '@caohenghu/vue-colorpicker'

export default {
  components: {
    colorPicker,
  },
  data() {
    return {
      color: '#59c7f9',
      suckerCanvas: null,
      suckerArea: [],
      isSucking: false,
    }
  },
  methods: {
    changeColor(color) {
      const {
        rgba: { r, g, b, a },
      } = color
      this.color = `rgba(${(r, g, b, a)})`
    },
    openSucker(isOpen) {
      if (isOpen) {
        // ... canvas be created
        // this.suckerCanvas = canvas
        // this.suckerArea = [x1, y1, x2, y2]
      } else {
        // this.suckerCanvas && this.suckerCanvas.remove
      }
    },
  },
}
</script>
