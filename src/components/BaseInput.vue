<template>
  <div class="input-wrap">
    <label v-if="label">{{ label }}</label>
    <input
      type="text"
      :value="modalValue"
      @input="$emit('update:modalValue', (<HTMLInputElement>$event.target).value)"
      v-bind="$attrs"
    />
  </div>
</template>

<script setup lang=ts>
defineProps({
  label: {
    type: [String, Boolean],
    default: false,
  },
  modalValue: {
    type: String,
    default: "",
  },
})
// use defineEmits macro when you want to add validation
</script>

<style lang="scss" scoped>
.input-wrap {
  display: flex;
  flex-direction: column;

  input {
    padding: 8px 12px;
    font-size: 16px;
  }
}
</style>