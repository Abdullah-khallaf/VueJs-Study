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
      }
}
</script>