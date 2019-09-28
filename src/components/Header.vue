<template>
    <div class="row">
        <div class="col-sm-12">
            <h3>Quotes Added</h3>
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (quoteCount / maxQuotes) * 100 + '%'}"><!--maens width is eg 6/10 *100 in percent. width will be equals to 60%-->
                        {{ quoteCount }} / {{ maxQuotes}} <!--eg 5/10-->
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>