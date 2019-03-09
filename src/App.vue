<template>
  <div class="container">
    <app-header :quotesCounts="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <new-quote @quoteAdded="newQuote"></new-quote>
    <quote-grid @quoteDeleted="deleteQuote" :quotes="quotes"></quote-grid>
      <div class="row footer text-center">
        <div class="col-sm-12 my-5 text-center">
          <div class="alert alert-info">Info: click on the quote do delete it!</div>
        </div>
      </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';

export default {
  name: 'app',

  data() {
    return {
      quotes: [
        'This is the first quote from the google.com'
      ],
      maxQuotes:10,
      
    }
  },
  components: {
    quoteGrid: QuoteGrid,
    newQuote: NewQuote,
    appHeader:Header
  },
  methods: {
    newQuote(quote) {
      if(this.quotes.length >= this.maxQuotes){
        return alert("delete some quotes")
      }
      
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.footer {
  position: fixed;
  bottom: 0;
  width: 65%;
  align-self: center;
}
</style>
