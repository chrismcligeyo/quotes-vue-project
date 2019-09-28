<template>
    <!--QuoteGrid displays all Quotes-->
    <div class="row">
        <!--loop through all quotes to render that single quote-->
        <app-quote v-for="quote in quotes">{{ quote }}</app-quote>
    </div>
</template>

<script>
    import Quote from './Quote';
    export default {
        //we need to be able to get array of quotes from outside. App.vue
        props: ['quotes'],
        components: {
            'app-quote':Quote
        }

    }
</script>

<style>

</style>