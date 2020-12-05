<template>
  <span class="badge">{{ title }}</span>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="css" scoped>
.badge {
    width: 100%;
    margin: 2% 0 4% 0;
    padding: 0;
    font-size: 30px;
    color: beige;
    background: gray;
}
</style>
