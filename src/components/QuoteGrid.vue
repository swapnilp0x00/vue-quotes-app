<template>
  <div class="row">
    List
    <appQuote v-for="quote in quotes" :key="quote"> {{ quote }}</appQuote>
  </div>
</template>

<script>
import Quote from "./Quote";
export default {
  components: {
    appQuote: Quote
  },
  props: ["quotes"]
};
</script>

<style lang="scss"></style>
