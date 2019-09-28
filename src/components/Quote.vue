<template>
 <div class="col-sm-6 col-md-4 col-lg-3">
     <div class="panel panel-default">
         <div class="panel-body quote">
             <slot></slot><!--bcoz quote content comes from outside. from holder of content. that is quotegrid-->
         </div>
     </div>
 </div>
</template>

<script>

</script>

<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: darkviolet;
    }

    .quote {
        cursor: pointer;

    }
    .qoute:hover{
        background-color: #ffe2e2;
    }

</style>