<template>
    <!--QuoteGrid displays all Quotes-->
    <div class="row">
        <!--loop through all quotes to render that single quote-->
        <app-quote v-for="(quote, index) in quotes" :key="quote" @click.native="deleteQuote(index)">{{ quote }}</app-quote><!--@click.native  will register a click on Quote.vue.if was just at click would not work -->
    </div>
</template>

<script>
    import Quote from './Quote';
    export default {
        //we need to be able to get array of quotes from outside. App.vue
        props: ['quotes'],
        components: {
            'app-quote':Quote
        },
        methods: {
            deleteQuote(index) {// need index to delete element
                this.$emit('quoteDeleted', index);//emit own event such that quotegrid communicates with parent App.vue.
            }

    }
    }
</script>

<style>

</style>