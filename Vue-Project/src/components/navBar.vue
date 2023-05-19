<template>
      <nav :class="navBarClasses">
      <ul>
        <li
          v-for=" (page, index) in pages"
          :key="index"
          :class="{active: activePage==index }"
        >
          <!--key is identifier for links to help vue know where it is-->
          <a
            :href="page.link.url"
            :title="`this link goes to ${page.link.text} page`"
            @click.prevent="activePage = index"
          >
            <!--How we bind data from the js-->
            <!--class will take the value active if the index is = activepage-->
            {{ page.link.text }}
          </a>
        </li>
      </ul>
      <form>
        <button class="btn-toggle" @click.prevent="useDarkNav = !useDarkNav">
          Background Toggle
        </button>
        <button class="btn-add" @click.prevent="addNumber()">
          click me to plus 1 {{ number }}
        </button>
      </form>
    </nav>
</template>

<script>
export default {
    computed: {
        navBarClasses() {
          return {
            darkNav: this.useDarkNav,
          };
        },
      },
      data() {
        //provide data to options
        return {
          activePage: 0,
          useDarkNav: false,
          number: 0,
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
      methods:{
        addNumber(){
          let number = this.number;
          number++;
          console.log(number);
        }
      }
}
</script>