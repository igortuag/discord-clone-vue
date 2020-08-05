<template>
  <div class="container">
    <div class="profile">
      <div class="profile__avatar"></div>
      <div class="userData">
        <strong class="userData_name">Igor Tuag</strong>
        <span class="userData_cod">#b246</span>
      </div>
    </div>

    <div class="actions">
      <Mic class="actions__icon" :size="20" />
      <HeadPhones class="actions__icon" :size="20" />
      <Settings class="actions__icon" :size="20" />
    </div>
  </div>
</template>

<script>
import Mic from 'vue-material-design-icons/Microphone';
import HeadPhones from 'vue-material-design-icons/Headphones';
import Settings from 'vue-material-design-icons/CogOutline';

export default {
  components: {
    Mic,
    HeadPhones,
    Settings
  }
};
</script>

<style lang="scss" scoped>
.container {
  grid-area: UI;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  background-color: var(--quaternary);
  box-shadow: rgba(0, 0, 0, 0.2) 0 1px 0 0;

  .profile {
    display: flex;
    align-items: center;

    &__avatar {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background-color: var(--gray);
    }
  }

  .userData {
    display: flex;
    flex-direction: column;
    margin-left: 8px;
    font-size: 13px;

    &_name {
      display: block;
      color: var(--white);
    }

    &_cod {
      color: var(--gray);
    }
  }

  .actions {
    color: var(--gray);

    &__icon {
      cursor: pointer;
      transition: 0.2s;

      &:hover {
        color: var(--white);
      }
    }
  }
}
</style>
