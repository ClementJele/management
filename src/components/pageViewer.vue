<template>
    <div  class="container ml-auto mt-3" >
        <h1> {{page.pageTitle}} </h1>
        <p> {{page.titleParagraph}} </p>
        
    </div>
    
</template>

<script>
export default {
 props: ['page']
}

</script>