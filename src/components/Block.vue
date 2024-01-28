<template>
  <div class="block">Click Here {{ delay }}</div>
</template>

<script>
export default {
  props: ["delay"],
};
</script>

<style>
.block {
  background: chocolate;
  width: 400px;
  height: 300px;
  margin: 20px auto;
  padding-top: 30px;
}
</style>
