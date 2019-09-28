<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote><!--@quteadded is custom event created in Newquote-->
    <!--we are passing the Quote array to the QuoteGrid-->
      <app-quote-grid :quotes="quotes"></app-quote-grid><!--App.vue is parent. :quotes is prop set so as to communicate with child QuoteGrid which has props:['quotes']-->
  <!--add info box-->
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>

import QuoteGrid from './components/QuoteGrid';
import NewQuote from './components/NewQuote.vue';
export default {
  data: function () {

    return {
      quotes: ['just something to see'], //quotes variable as an arry
      maxQuotes: 10
    }

  },
  components: {
    'app-quote-grid': QuoteGrid,
    'app-new-quote': NewQuote
  },
  methods: {
    newQuote(quote) {// this.$emit('quoteAdded', this.quote); this.quote is the quote in newQuote(quote) . This is would be done as if it wer above <app-new-quote @quoteAdded="newQuote($event)"></app-new-quote> $event being this.quote

      this.quotes.push(quote);

  }
}
}

</script>

<style>

</style>
