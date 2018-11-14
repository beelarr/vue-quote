<template>
    <div class="container">
        <new-quote @quoteAdded="postNewQuote"></new-quote>
        <quote-grid :quotes="quotes" ></quote-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';

    export default {
        data: () => ({
            quotes: [
                'Just a quote to see.'
            ],
            maxQuotes: 10
          }),
      methods: {
        	postNewQuote(quote){
        		this.quotes.push(quote)
          }
      },
      components: {
        	quoteGrid: QuoteGrid,
          newQuote: NewQuote
      }
    }
</script>

<style>
</style>
