<template>
  <div>
    <h2 class="subtitle">
      Where were you born?
    </h2>

    <div>
      <input v-model="answers.place" type="text">
    </div>

    <div class="actions">
      <button class="button" @click="advance">
        {{ answers.place.length ? 'Go!' : 'Choose for me' }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InterviewPlace',

  props: {
    answers: {
      type: Object,
      required: true
    }
  },

  methods: {
    advance() {
      if (!this.answers.place) {
        this.answers.place = 'Venice'
      }

      this.$emit('advance')
    }
  }
}
</script>
