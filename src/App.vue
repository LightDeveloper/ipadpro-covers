<template>
    <div class="container">
        <progress-header :numberOfQuotes="quotes.length"></progress-header>
        <new-quote
                @newQuoteCreated="newQuoteCreated"
        ></new-quote>
        <p></p>
        <quotes :quotes="quotes" @deleteQuoteAtIndex="deleteQuoteAtIndex"></quotes>
        <p></p>
        <div class="alert alert-info text-center" role="alert">Info: Click on a quote to delete it</div>
    </div>
</template>

<script>
    import ProgressHeader from './components/ProgressHeader.vue'
    import NewQuote from './components/NewQuote.vue'
    import Quotes from './components/Quotes.vue'
    export default {
        components: {
            ProgressHeader,
            NewQuote,
            Quotes
        },
        data() {
            return {
                quotes: [ ]
            };
        },
        created() {
            console.log("App created");
        },
        methods: {
            newQuoteCreated(quote) {
                if (this.quotes.length >= 10) {
                    alert('Cannot add more than 10 quotes')
                } else {
                    this.quotes.push(quote);
                }
            },
            deleteQuoteAtIndex(index) {
                this.quotes.splice(index, 1);
            }
        }
    }

</script>

<style>
</style>
