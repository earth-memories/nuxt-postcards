<template>
  <figure>
    <figcaption>{{ year }} {{ place }} {{ season }}</figcaption>
    <img src="https://placeimg.com/640/480/arch/sepia">
  </figure>
</template>

<script>
export default {
  name: 'Postcard',
  props: {
    year: { type: Number, required: true },
    place: { type: String, required: true },
    season: { type: String, required: true }
  }
}
</script>
