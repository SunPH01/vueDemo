<template>
  <div class="main-wrapper">
    <Header />
    <div class="main-body">
      <Menu />
      <div class="main-content"><router-view> </router-view></div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Header from "./Header.vue";
import Menu from "./Menu.vue";
export default defineComponent({
  components: { Header, Menu },
});
</script>
<style lang="less" scoped>
.main-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
}
.main-body {
  flex: 1;
  display: flex;
  background-color: @background-color-base;
  .main-content {
    flex: 1;
    margin: 16px;
    padding: 16px;
    background-color: @component-background;
  }
}
</style>
