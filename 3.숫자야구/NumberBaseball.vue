<template>
  <div>
    <h1>{{ result }}</h1>
    <form action="">
      <input type="text" ref="answer" maxlength="4" v-model="value">
      <button @click="onSubmitForm">입력</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "NumberBaseball",
  data() {
    return {
      result: '',
      value: ''
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
