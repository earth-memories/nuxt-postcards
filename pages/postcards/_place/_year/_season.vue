<template>
  <section class="container">
    <ol>
      <li v-for="year in years" :key="year">
        <Postcard :year="year" :place="place" :season="season" />
      </li>
    </ol>
  </section>
</template>

<script>
import Postcard from './Postcard'

export default {
  components: { Postcard },
  computed: {
    years() {
      return [Number(this.$route.params.year), new Date().getFullYear(), 2050]
    },

    place() {
      return this.$route.params.place
    },
    season() {
      return this.$route.params.season
    }
  }
}
</script>
