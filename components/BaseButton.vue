<template>
  <button class="button">
    <slot />
  </button>
</template>

<script>
export default {
  name: 'BaseButton',
}
</script>

<style lang="scss" scoped>
.button {
  padding: 1rem 2rem;
  background-color: var(--green-500);
  color: var(--gray-300);
  border-radius: 4px;
  border: 0;

  font-size: 1rem;
  font-weight: 500;

  transition: filter 200ms;

  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.625rem;

  &:hover {
    filter: brightness(0.9);
  }
}
</style>
