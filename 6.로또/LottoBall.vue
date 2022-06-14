<template>
  <div>
    <div class="ball" :style="{ background }">
      {{ number }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'LottoBall',
  components: {},
  data() {
    let background;
    return {
      background,
    }
  },
  props: {
    number: {
      type: Number
    }
  },
  computed: {},
  watch: {},
  methods: {}
}
</script>

<style>
.ball {
  display: inline-block;
  border: 1px solid black;
  border-radius: 20px;
  width: 40px;
  height: 40px;
  line-height: 40px;
  font-size: 20px;
  text-align: center;
  margin-right: 20px;
}
</style>
