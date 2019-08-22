<template>
  <div>
    <h2 class="subtitle">
      How old are you?
    </h2>

    <div>
      <input v-model="answers.age" type="number">
    </div>

    <div class="actions">
      <button class="button" @click="$emit('advance')">
        Go!
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InterviewAge',

  props: {
    answers: {
      type: Object,
      required: true
    }
  }
}
</script>
