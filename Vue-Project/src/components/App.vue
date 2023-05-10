<template>
    <navBar></navBar>
    <page-viewer :page="pages[activePage]"></page-viewer>
</template>

<script>
import navBarVue from './navBar.vue';
import pageViewer from './components/pageViewer.vue';


export default {

  components:{
    navBarVue,
    pageViewer,
  },
    data() {
        //provide data to options
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
            }
          ]
        };
    },
}
</script>