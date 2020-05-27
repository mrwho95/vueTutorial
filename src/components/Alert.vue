<template>
  <div>
    <div class="alert" :class="mode" role="alert">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Alert",
  //   props can accept object, array
  props: ["mode"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.primary {
  color: #004085;
  background-color: #cce5ff;
  border-color: #b8daff;
}

.success {
  color: #155724;
  background-color: #d4edda;
  border-color: #c3e6cb;
}

.danger {
  color: #721c24;
  background-color: #f8d7da;
  border-color: #f5c6cb;
}

.alert {
  position: relative;
  padding: 0.75rem 1.25rem;
  margin-bottom: 1rem;
  border: 1px solid transparent;
  border-radius: 0.25rem;
}
</style>
