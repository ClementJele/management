<template>
 <navbar
    :pages = "pages"
    :active-page = "activePage"
    :nav-link-click = "(index) => activePage = index"
    >
  </navbar>
   

    <page-viewer
    :page = "pages[activePage]"
    ></page-viewer>
</template>

<script>

import pageViewer from './components/pageViewer.vue';
import Navbar from './components/Navbar.vue';

export default {
  components : {
    
    Navbar,
    pageViewer
  },


  data() {
    return {
      activePage: 1,

      pages: [
        {
          link: { text: "Home", url: "index.html" },
          pageTitle: "Home Page",
          titleParagraph: "Welcome to the home page",
        },

        {
          link: { text: "About", url: "about.html" },
          pageTitle: "About Page",
          titleParagraph: "Welcome to the about page",
        },

        {
          link: { text: "Contacts", url: "contacts.html" },
          pageTitle: "Contacts Page",
          titleParagraph: "Welcome to vue",
        },

        {
          link: { text: "Pricing", url: "pricing.html" },
          pageTitle: "Pricing Page",
          titleParagraph: "Welcome to vue",
        },

        {
          link: { text: "Promotions", url: "promotions.html" },
          pageTitle: "Promotions Page",
          titleParagraph: "Welcome to vue",
        },

        {
          link: { text: "Products", url: "products.html" },
          pageTitle: "Products Page",
          titleParagraph: "Welcome to vue",
        },
      ],
    };
  },
};
</script>
