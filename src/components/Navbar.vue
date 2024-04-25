
<template> 
    <nav class="navbar navbar-expand-lg bg-dark navbar-dark">
             <div class="container-fluid">
                 <a class="navbar-brand">
                     My Vue App
                 </a>
     
                 <ul class="navbar-nav me-auto mb-2 mb-lg-0 " >
                     <li v-for="(page, index) in pages" class="nav-item" :key="index" >
                         <a 
                         class="nav-link" 
                         :class="{active: activepage == index}"
                         aria-current="page" 
                         :href="page.link.url"
                         :title= "`This link goes to the ${page.link.text} page`"
                         @click.prevent="navLinkClick(index)"
                         >
                             {{ page.link.text }}
                             
                         </a>
                     </li>
                 </ul>
             </div>
         </nav></template>
    
    <script>
    export default {
    
       
     props:['pages', 'activePage', 'navLinkClick'],
     
    }
    
    </script>
    