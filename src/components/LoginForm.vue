<template>
  <form @submit.prevent="onSubmit">
    <input type="text" data-testid="name-input"  v-model="name" />
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('formSubmitted', { name: this.name })
    }
  }
}
</script>