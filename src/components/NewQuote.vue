<template>
    <div class="row">
        <form>
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
                <label>Quote</label>
                <textarea v-model="quoteText" class="form-control" rows="3"></textarea>
            </div>
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
                <button @click.prevent="addQuote" class="btn btn-primary center-block">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quoteText: ''
            };
        },
        methods: {
            addQuote() {
                const quote = this.quoteText.trim();
                if (quote.length === 0) {
                    console.log('Cannot add empty quote');
                    return;
                }

                this.$emit('newQuoteCreated', quote);
                this.quoteText = '';
            }
        }
    }
</script>

<style>

</style>
