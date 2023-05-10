<template>
  <div style="text-align: center">
    <h1>{{ page.pageTitle }}</h1>
    <p>{{ page.content }}</p>
  </div>
</template>

<script>
export default {
  props: ["page"],
};
</script>
