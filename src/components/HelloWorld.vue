<template>
  <div class="hello">
    <h3 class="text-red-400">{{ msg }}</h3>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "HelloWord",
  props: {
    msg: String
  },
  data: () => {
    return {
      count: 1
    };
  }
});
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
</style>
