<template>
  <section class="container">
    <component :is="stageComponent" :answers="answers" @advance="advance" />
  </section>
</template>

<script>
import InterviewAge from '../components/InterviewAge'
import InterviewPlace from '../components/InterviewPlace'
import InterviewSeason from '../components/InterviewSeason'

const COMPONENTS = [InterviewAge, InterviewPlace, InterviewSeason]

export default {
  data() {
    return {
      answers: {
        age: 30,
        place: '',
        season: ''
      },

      stage: 0
    }
  },

  computed: {
    stageComponent() {
      return COMPONENTS[this.stage]
    },

    year() {
      return new Date().getFullYear() - this.answers.age
    }
  },

  methods: {
    advance() {
      this.stage += 1

      if (this.stage >= COMPONENTS.length) {
        this.$router.push(
          `/postcards/${this.answers.place}/${this.year}/${this.answers.season}`
        )
      }
    }
  }
}
</script>
