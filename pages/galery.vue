<template>
  <div>
    <div class="container" id="app">
      <VueGalery></VueGalery>
    </div>
  </div>
</template>

<script>
import VueGalery from '@/components/VueGalery'
export default {
  components: { VueGalery },
  data() {
    return {
      photos: [
        "'@/static/0.jpg'",
        "'@/static/1.jpg'",
        "'@/static/2.jpg'",
        "'@/static/3.jpg'",
        "'@/static/4.jpg'",
        "'@/static/5.jpg'",
        "'@/static/6.jpg'",
        "'@/static/7.jpg'",
        "'@/static/8.jpg'",
        "'@/static9.jpg'",
      ],
    }
  },
}
</script>

<style lang="scss">
.container {
  padding: 6px;
  background-color: #fff;
  border-radius: 8px;
  max-width: 800px;
  box-shadow: 0 5px 8px #0000007a;
}
</style>
