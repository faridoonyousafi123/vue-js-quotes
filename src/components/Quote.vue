<template>
   <div class="col-sm-6 col-md-4 col-offset-3 col-lg-3 my-2">
       <div class="panel panel-default">
           <div class="panel-body quote">
               <slot></slot>
           </div>
       </div>
   </div>
</template>

<script>
export default {

}
</script>

<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color:white;
        background-color: #5d5229;
        text-align: center;
        padding: 10px;
        border-radius: 10px;
    }
    .quote {
        cursor: pointer;
    }
    .quote:hover{
        background-color:#8c8053;
    }
</style>
