<template>
  
</template>

<script>
import Navbar from './components/Navbar.vue';
import PageViewer from './components/PageViewer.vue';

export default {
components: {
  Navbar,
  PageViewer,
},
data() {
  return {
    activePage: 0,
    useDarkNav: false,
    pages: [
      {
        link: { text: "Home", url: "index.html" },
        pageTitle: "Home",
        content: "This Home Page",
      },
      {
        link: { text: "About", url: "about.html" },
        pageTitle: "About",
        content: "This About Page",
      },
      {
        link: { text: "Contact", url: "contact.html" },
        pageTitle: "Contact",
        content: "This Contact Page",
      },
    ],
  };
},
}
</script>
