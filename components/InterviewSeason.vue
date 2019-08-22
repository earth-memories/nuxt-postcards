<template>
  <div>
    <h2 class="subtitle">
      Which season do you prefer?
    </h2>

    <div class="actions">
      <button class="button" @click="choose('winter')">
        Winter
      </button>

      <button class="button" @click="choose('summer')">
        Summer
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InterviewSeason',

  props: {
    answers: {
      type: Object,
      required: true
    }
  },

  methods: {
    choose(season) {
      this.answers.season = season
      this.$emit('advance')
    }
  }
}
</script>
