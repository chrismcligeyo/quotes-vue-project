<template>
  <div class="container">
    <!--we are passing the Quote array to the QuoteGrid-->
      <app-quote-grid :quotes="quotes"></app-quote-grid><!--App.vue is parent. :quotes is prop set so as to communicate with child QuoteGrid which has props:['quotes']-->
  </div>
</template>

<script>

import QuoteGrid from './components/QuoteGrid'
export default {
  data: function () {

    return {
      quotes: ['just something to see'], //quotes variable as an arry
      maxQuotes:10
    }

  },
  components: {
    'app-quote-grid': QuoteGrid
  }
}
</script>

<style>

</style>
