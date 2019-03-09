<template>
    <div class="row my-5">
        <div class="col-sm-12">
            <h3>Quotes Added</h3>
              
                    <div class="progress">
                        <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (quotesCounts / maxQuotes) * 100 +'%'}">
                            {{ quotesCounts }} / {{ maxQuotes }}
                        </div>
                    </div>
            
        </div>
    </div>
</template>

<script>
export default {

    props:['quotesCounts', 'maxQuotes']
}
</script>

<style scoped>

    .progress{
        height: 20px !important;
    }
    .progress-bar {
        font-size: 15px;
    }

</style>
