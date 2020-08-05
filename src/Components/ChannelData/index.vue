<template>
  <div class="channel-data">
    <div class="messages">
      <ChannelMessages author="Dyno" date="04/08/2020" isBot hasMention>
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Poly Tuag" date="04/08/2020">
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Igor Tuag" date="04/08/2020" hasMention>
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Dyno" date="04/08/2020" isBot>
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Igor Tuag" date="05/08/2020">
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Poly Tuag" date="05/08/2020" hasMention>
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Igor Tuag" date="05/08/2020">
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Dyno" date="05/08/2020" isBot>
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages
        v-for="messages in 18"
        :key="messages.id"
        author="User"
        date="05/08/2020"
      >
        Está é uma mensagem de teste
      </ChannelMessages>
      <ChannelMessages author="Igor Tuag" date="05/08/2020" hasMention>
        <Mention>User</Mention>, olha só isso!
      </ChannelMessages>
    </div>
    <div class="inputWrapper">
      <input
        type="text"
        class="inputWrapper__input"
        placeholder="Conversar em #chat-livre"
      />
      <div class="inputWrapper__icon">
        <At :size="24" />
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import At from 'vue-material-design-icons/At';
import ChannelMessages from './ChannelMessages';

export default {
  components: {
    At,
    ChannelMessages
  }
};

Vue.component('Mention', {
  template: '<span class="mention"><slot /></span>'
});
</script>

<style lang="scss" scoped>
.channel-data {
  grid-area: CD;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: var(--primary);
  flex: 1;
}

.messages {
  display: flex;
  flex-direction: column;
  height: calc(100vh - 46px - 68px);
  max-height: calc(100vh - 46px - 68px);
  overflow-y: scroll;

  .channelMessage:first-child {
    margin-top: 0;
  }

  &::-webkit-scrollbar {
    width: 8px;
  }

  &::-webkit-scrollbar-thumb {
    background-color: var(--tertiary);
    border-radius: 4px;
  }

  &::-webkit-scrollbar-track {
    background-color: var(--secondary);
  }
}

.inputWrapper {
  width: 100%;
  padding: 0 16px;
  height: 68px;

  &__input {
    width: 100%;
    height: 44px;
    padding: 0 10px 0 57px;
    border-radius: 5px;
    color: var(--white);
    background-color: var(--chat-input);
    position: relative;

    &::placeholder {
      color: var(--gray);
    }
  }
  &__icon {
    color: var(--gray);
    position: relative;
    top: -50%;
    left: 14px;
    transition: 0.2s;
    width: 24px;
  }
}
</style>
