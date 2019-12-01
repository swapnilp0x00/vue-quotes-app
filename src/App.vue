<template>
  <div id="container">
    <appHeader :maxQuotes="maxQuotes" :quoteCount="quotes.length"></appHeader> 
    <appNewQuote @quoteAdded="newQuote"></appNewQuote>
    <appQuoteGrid :quotes="quotes" @deleteQuote="deleteQuote"></appQuoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on a Quote to delete this !
        </div> 
      </div> 
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";
export default {
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  },
  data () {
    return {
      maxQuotes: 10,
      quotes: ['Sample', 'Sample 2']
    }
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("Full");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style lang="scss">

</style>
