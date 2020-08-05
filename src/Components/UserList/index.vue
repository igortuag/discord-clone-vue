<template>
  <div class="userList">
    <div class="role">Disponivel - 1</div>
    <UserRow nickname="Igor Tuag" />
    <UserRow nickname="Dyno" isBot />
    <div class="role">Offline - 18</div>
    <UserRow nickname="Poly Tuag" />
    <UserRow nickname="Edu Cavalheiro" />
    <UserRow nickname="Tiago Emanuel" />
    <UserRow nickname="Carlitos" isBot />
    <UserRow nickname="João Correia" />
    <UserRow nickname="Ana" />
    <UserRow nickname="Julia" />
    <UserRow nickname="Pedro" />
    <UserRow nickname="Paulo" />
    <UserRow nickname="Destructor" />
    <UserRow nickname="Junin" />
    <UserRow nickname="F3nix-lol Br tremetudo doido" />
    <UserRow nickname="Jean" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
    <UserRow nickname="User" />
  </div>
</template>

<script>
import UserRow from './UserRow';

export default {
  components: {
    UserRow
  }
};
</script>

<style lang="scss" scoped>
.userList {
  grid-area: UL;
  display: flex;
  flex-direction: column;
  padding: 3px 6px 10px 16px;
  background-color: var(--secondary);
  max-height: calc(100vh - 46px);
  overflow-y: scroll;

  &::-webkit-scrollbar {
    width: 4px;
  }

  &::-webkit-scrollbar-thumb {
    background-color: var(--tertiary);
    border-radius: 4px;
  }

  &::-webkit-scrollbar-track {
    background-color: var(--secondary);
  }
}

.role {
  margin-top: 20px;
  color: var(--gray);
  font-weight: 500;
  font-size: 12px;
  text-transform: uppercase;
}
</style>
