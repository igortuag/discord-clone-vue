<template>
  <div class="container">
    <div class="container__icon"><Hashtag :size="24" /></div>
    <h1 class="container__title">chat-livre</h1>
    <div class="container__separator"></div>
    <div class="container__description">Canal aberto para conersas</div>
  </div>
</template>

<script>
import Hashtag from 'vue-material-design-icons/Pound';

export default {
  components: {
    Hashtag
  }
};
</script>

<style lang="scss" scoped>
.container {
  grid-area: CI;
  background-color: var(--primary);
  display: flex;
  align-items: center;
  padding: 0 17px;
  box-shadow: rgba(0, 0, 0, 0.9) 0 1px 0 0;
  z-index: 2;

  &__title {
    color: var(--white);
    font-size: 16px;
    margin-left: 9px;
    font-weight: bold;
  }

  &__description {
    color: var(--gray);
    font-size: 15px;
  }

  &__separator {
    background-color: var(--white);
    height: 24px;
    width: 1px;
    opacity: 0.2;
    margin: 0 13px;
  }

  &__icon {
    color: var(--symbol);
  }
}
</style>
