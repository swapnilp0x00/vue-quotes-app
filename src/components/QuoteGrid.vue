<template>
  <div class="row">
    <appQuote v-for="(quote, index) in quotes" :key="quote" @click.native="deleteQuote(index)"> {{ quote }}</appQuote>
  </div>
</template>

<script>
import Quote from "./Quote";
export default {
  components: {
    appQuote: Quote
  },
  props: ["quotes"],
  methods : {
      deleteQuote(index) {
          this.$emit('deleteQuote', index);
      }
  }
};
</script>

<style lang="scss"></style>
