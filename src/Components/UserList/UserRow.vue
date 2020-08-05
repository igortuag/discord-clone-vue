<template>
  <div class="userRow">
    <div
      class="userRow__avatar"
      :class="{ 'userRow__avatar--isBot': isBot }"
    ></div>
    <strong class="userRow__name">{{ nickname }}</strong>
    <div class="userRow__bot" v-if="isBot">Bot</div>
  </div>
</template>

<script>
export default {
  props: {
    nickname: String,
    isBot: Boolean
  }
};
</script>

<style lang="scss" scoped>
.userRow {
  display: flex;
  margin-top: 5px;
  padding: 5px;
  align-items: center;
  cursor: pointer;
  border-radius: 5px;
  background-color: transparent;
  transition: 0.2s;

  &:hover {
    background: rgba(255, 255, 255, 0.1);
  }

  &__name {
    margin-left: 13px;
    font-weight: 500;
    color: var(--white);
    opacity: 0.7;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
  }

  &__avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    flex-shrink: 0;
    background-color: var(--primary);

    &--isBot {
      background: var(--mention-detail);
    }
  }

  &__bot {
    margin-left: 9px;
    background-color: var(--discord);
    color: var(--white);
    padding: 4px 5px;
    border-radius: 4px;
    text-transform: uppercase;
    font-size: 11px;
    font-weight: bold;
  }
}
</style>
