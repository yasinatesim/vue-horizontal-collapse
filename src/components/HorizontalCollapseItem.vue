<template>
  <li
    v-on-clickaway="away"
    @click="isActive = !isActive"
    :style="
      `width: ${
        isActive ? itemMaxWidth : itemMinWidth
      }px;min-width: ${itemMinWidth}px;max-width: ${itemMaxWidth}px`
    "
    class="js-horizontal-collapse-item  horizontal-collapse__item"
    :class="{ 'is-active': isActive, [className]: true }"
    tabindex="0"
    role="button"
  >
    <div
      :style="`width: ${itemMaxWidth}px`"
      class="js-horizontal-collapse-item-inner  horizontal-collapse__item-inner"
    >
      <slot></slot>
    </div>
  </li>
</template>

<script>
import { mixin as clickaway } from "vue-clickaway";

export default {
  name: "HorizontalCollapseItem",
  mixins: [clickaway],
  data() {
    return {
      isActive: false,
      itemMinWidth: 150,
      itemMaxWidth: 500
    };
  },
  methods: {
    away() {
      this.isActive = false;
    }
  },
  props: ["className"]
};
</script>

<style></style>
