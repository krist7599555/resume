<template>
  <a :href="href" target="_blank" rel="noopener noreferrer">
    <figure class="image">
      <video v-if="video" controls autoplay>
        <source
          src="https://instagram.fbkk22-3.fna.fbcdn.net/v/t50.2886-16/28689620_1872395129478431_8944262208439713792_n.mp4?_nc_ht=instagram.fbkk22-3.fna.fbcdn.net&_nc_cat=111&oe=5DA012EA&oh=5e6c6ec44eeff335a9bfb3b4b30d805e"
          type="video/mp4"
        />
      </video>
      <img v-else :src="src" :alt="alt" />
      <!-- <figcaption>{{alt}}</figcaption> -->
      <br />
    </figure>
  </a>
</template>

<script>
export default {
  props: {
    href: { type: String, default: '' },
    src: { type: String, default: '' },
    alt: { type: String, default: '' },
    video: { type: Boolean, default: false }
  }
}
</script>

<style lang="scss" scoped>
img,
video {
  // padding: 5px;
  border: solid 1px white;
  border-top-width: 0;
  border-radius: 0 0 4px 4px;
}
figcaption {
  text-align: center;
  font-size: 0.8rem;
  margin-top: 6px;
  margin-bottom: 16px;
}
</style>
