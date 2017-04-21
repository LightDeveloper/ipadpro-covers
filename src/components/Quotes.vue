<template>
    <div class="row">
        <div class="col-sm-3" v-for="(quote, index) in quotes">
            <quote :index="index"
                   @click.native="deleteQuoteAtIndex(index)">
                {{ quote }}
            </quote>
        </div>
    </div>
</template>

<script>
    import Quote from './Quote.vue'
    export default {
        components: {
            Quote
        },
        props: ['quotes'],
        methods: {
            deleteQuoteAtIndex(index){
                this.$emit('deleteQuoteAtIndex', index);
            }
        }
    }
</script>

<style>

</style>
