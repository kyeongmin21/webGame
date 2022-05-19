<template>
  <div>
    <h1>{{ result }}</h1>
    <form action="">
      <input type="text" v-model="value">
      <button @click="onSubmitForm">입력</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "NumberBaseball.vue",
  data() {
    return {
      value: '',
      result: ''
    }
  },
  methods: {
    onSubmitForm (e) {
      e.preventDefault()
    }
  }
}
</script>

<style scoped>

</style>
