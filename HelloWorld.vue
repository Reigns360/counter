<template>
  <div class="counter">
    <v-btn color="primary" @click="decrement" class="mr-2">-</v-btn>
    <span class="count">{{ count }}</span>
    <v-btn color="primary" @click="increment" class="ml-2">+</v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    }
  }
};
</script>

<style scoped>
.counter {
  display: flex;
  align-items: center;
  justify-content: center;
}

.count {
  font-size: 2em;
  margin: 0 20px;
}
</style>
