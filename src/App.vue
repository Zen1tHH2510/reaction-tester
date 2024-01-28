<template>
  <div style="text-align: center" class="">
    <h1 class="hero-header">Test your reaction speed.</h1>
    <br />
    <button @click="start" :disabled="isPlaying">Play</button>
    <br />
    <div v-if="isPlaying">
      <Block :delay="delay" />
    </div>
  </div>
</template>

<script>
import Block from "./components/Block.vue";
export default {
  components: {
    Block,
  },
  data() {
    return {
      isPlaying: false,
      delay: null,
    };
  },
  methods: {
    start() {
      this.isPlaying = true;
      this.delay = 2000 + Math.random() * 5000;
    },
  },
};
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
.hero-header {
  text-align: center;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
