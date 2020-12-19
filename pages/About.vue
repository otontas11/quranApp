<template>
  <div>
    <div>
      <b-embed
        type="iframe"
        aspect="16by9"
        :src="link"
        allowfullscreen
      ></b-embed>

      <div>
        <h3 class="text-center black">
          <b-link
            href="https://play.google.com/store/apps/details?id=platform.tnts.tecvidogren&hl=tr"
            target="_blank"
            >Link to Download this app</b-link
          >
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      link: 'https://www.youtube.com/embed/6B9NEGz7ZTU',
    }
  },
}
</script>

<style lang="scss" scoped></style>
