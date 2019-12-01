<template>
  <div id="container">
    App
    <appQuoteGrid :quotes="quotes"></appQuoteGrid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
export default {
  components: {
    appQuoteGrid: QuoteGrid
  },
  data () {
    return {
      maxQuotes: 10,
      quotes: ['Sample', 'Sample 2']
    }
  }
};
</script>

<style lang="scss">

</style>
