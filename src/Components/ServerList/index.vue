<template>
  <div class="container">
    <ServerButton isHome />
    <div class="separator" />
    <ServerButton :mentions="3" />
    <div class="separator" />
    <ServerButton hasNotification />
    <div class="separator" />
    <ServerButton :mentions="32" hasNotification />
    <div class="separator" />
    <ServerButton />
    <div class="separator" />
    <ServerButton />
    <div class="separator" />
    <ServerButton :mentions="4" hasNotification />
    <div v-for="servers in 18" :key="servers.id">
      <div class="separator" />
      <ServerButton />
    </div>
  </div>
</template>

<script>
import ServerButton from './ServerButton';

export default {
  components: {
    ServerButton
  }
};
</script>

<style lang="scss" scoped>
.container {
  grid-area: SL;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--tertiary);
  padding: 11px 0;
  max-height: 100vh;
  overflow-y: scroll;

  &::-webkit-scrollbar {
    display: none;
  }
}

.separator {
  width: 32px;
  border-bottom: solid 2px var(--quaternary);
  margin-bottom: 8px;
}
</style>
