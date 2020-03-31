<template>
  <div class="tab"></div>
</template>

<script>
export default {
  name: 'TabBlock'
};
</script>

<style scoped>
.tab {
  height: 6rem;
  margin: auto;
  background-color: aqua;
  border-radius: 0.5rem;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  transition: background-color ease 0.2s;
}

.tab:hover {
  background-color: aquamarine;
  transition: background-color ease 0.2s;
}
</style>
