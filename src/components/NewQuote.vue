<template>
    <div class="row my-3">
        <form>
            <div class="col-lg-12 offset-md-6 form-group">
                <label>Quote</label>
                <textarea name="" id="" cols="60" rows="3" class="form-control" v-model="quote"></textarea>
            </div>

            <div class="col-lg-12 offset-md-6 form-group">
                <button :disabled="isEmpty" class="btn btn-primary" @click.prevent="createNewQuote">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            quote: '',
        
        }
       
    },
    methods: {
        createNewQuote() {
            this.$emit('quoteAdded', this.quote);
            this.quote = '';
        }
    },
    computed: {
        isEmpty(){

                return !this.quote;
           }
    }
}
</script>

<style>

</style>
