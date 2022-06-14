<template>
  <div>
    <h3>당첨 숫자</h3>
    <div id="result">
      <LottoBall v-for="ball in winBalls" number="5" />
    </div>
    <h3>보너스</h3>
    <LottoBall v-if="bonus"/>
    <button v-if="redo">한번더</button>
  </div>
</template>

<script>
import LottoBall from "./LottoBall";

export default {
  name: 'LottoGenerator',
  components: {
    LottoBall
  },
  data() {
    return {
      // 미리 숫자들을 뽑아놓고
      winNumbers: this.getWinNumbers(),
      // 시각적인 용도로 하나씩 추가하는 역할
      winBalls: [],
      bonus: null,
      redo: false,

    }
  },
  computed: {},
  watch: {},
  mounted() {
    for (let i = 0; i < this.winNumbers.length; i++) {
      setTimeout(() => {
        this.winBalls.push(this.winNumbers[i])
      }, (i + 1) * 1000)
    }
  },
  methods: {
    getWinNumbers() {
      const candidate = Array(45).fill().map((value, index) => index + 1);
      const shuffle = [];
      while (candidate.length > 0) {
        shuffle.push(candidate.splice(Math.Trunk(Math.random() * candidate.length), 1)[0]);
      }

      const bonusNumber = shuffle[shuffle.length - 1];
      const winNumbers = shuffle.slice(0, 6).sort((a, b) => a - b);
      return [...winNumbers, bonusNumber];
    }
  }
}
</script>

<style>

</style>
