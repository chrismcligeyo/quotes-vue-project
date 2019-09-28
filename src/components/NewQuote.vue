<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea><!--two way binding.-->
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
               <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button><!--@click.prevent, prevents default behavior. dont want to submitform tht will reload page-->
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quote: '' //binding from text area
            };
        },
        methods: {
            //when you create new we want to add NewQuote to parent element App.vue
            createNew() { //emit new quote. connects NewQuote childto parent container App.vue. whatever you add when click button will be displayed in parent container too
                this.$emit('quoteAdded', this.quote);
                //clearform after adding quote
                this.quote = '';
            }
        }
    }
</script>

<style>

</style>