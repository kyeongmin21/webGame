<template>
  <div>
    <h3>당첨 숫자</h3>
    <div id="result">
      <LottoBall v-for="ball in winBalls"/>
    </div>
    <h3>보너스</h3>
    <LottoBall v-if="bonus"/>
    <button v-if="redo">한번더</button>
  </div>
</template>

<script>
export default {
  name: 'LottoBall',
  components: {},
  data() {
    return {
      winBalls: [],
      bonus: null,
      redo: false,

    }
  },
  computed: {},
  watch: {},
  methods: {}
}
</script>

<style>

</style>
