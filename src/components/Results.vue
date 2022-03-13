<template>
  <p >Reaction time: {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 100) {
      this.rank = 'Extreme speed!'
    } else if (this.score < 250) {
      this.rank = 'Great speed!'
    } else if (this.score < 500) {
      this.rank = 'Could be better.'
    } else {
      this.rank = 'Oh, dear...'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>