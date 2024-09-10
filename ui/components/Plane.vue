<template>
  <div :style="'z-index:'+level" class="planeBlock">
    <div :style="'left: ' + plane.x + '%; top: ' + plane.y + '%; transform: rotate(' + (plane.angle - 180) + 'deg);'"
         class="icon">
      &#9992;
    </div>
    <div :style="'left: ' + plane.x + '%; top: ' + plane.y + '%;'" class="title">{{ plane.name }}</div>
  </div>
</template>
<script>
export default {
  props: {
    level: 0,
    plane: null
  }

}
</script>
<style>
.planeBlock {
  width: 100%;
  min-height: 100vh;
  position: absolute;
}

.planeBlock .icon {
  position: absolute;
  font-size: 300%;
  color: #ffffff;
  transform-origin: center center;
}

.planeBlock .title {
  position: absolute;
  background: #232323;
  color: chartreuse;
  padding: 2px 5px;
  text-align: center;
}
</style>
