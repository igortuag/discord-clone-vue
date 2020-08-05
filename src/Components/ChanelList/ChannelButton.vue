<template>
  <div class="chanelList" :class="{ 'chanelList--active': selected }">
    <div class="chanelInfo">
      <div class="chanelInfo__icon">
        <HashTagIcon :size="20" />
      </div>
      <div class="chanelInfo__name">
        {{ channelName }}
      </div>
    </div>
    <div class="chanelActions">
      <InviteIcon class="chanelActions__icons" :size="16" />
      <SettingsIcon class="chanelActions__icons" :size="16" />
    </div>
  </div>
</template>

<script>
import HashTagIcon from 'vue-material-design-icons/Pound';
import InviteIcon from 'vue-material-design-icons/AccountPlus';
import SettingsIcon from 'vue-material-design-icons/CogOutline';

export default {
  components: {
    HashTagIcon,
    InviteIcon,
    SettingsIcon
  },
  props: {
    channelName: String,
    selected: Boolean
  }
};
</script>

<style lang="scss" scoped>
.chanelList {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  cursor: pointer;
  padding: 5px 3px;
  border-radius: 5px;
  background-color: transparent;

  > div {
    display: flex;
    align-items: center;
  }

  .chanelInfo {
    &__name {
      color: var(--senary);
      margin-left: 5px;
    }

    &__icon {
      color: var(--symbol);
    }
  }

  .chanelActions {
    display: none;
    &__icons {
      color: var(--symbol);
      margin-left: 4px;
      transition: 0.2s;
      &:hover {
        color: var(--white);
      }
    }
  }

  &:hover,
  &--active {
    background-color: var(--quinary);
    .chanelInfo {
      &__name {
        color: var(--white);
      }
    }
    .chanelActions {
      display: flex;
    }
  }
}
</style>
