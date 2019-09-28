<template>
    <div class="row">
        <div class="col-sm-12">
            <h3>Quotes Added</h3>
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (quoteCount / maxQuotes) * 100 + '%'}"><!--set width to eg 5/10 8100 = 0.5 in percentage is 50%, so here we are setting the width to whtevever value is quotecount / maxqoutes in %-->
                        {{ quoteCount }} / {{ maxQuotes}} <!--will display something like 5/10-->
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