<template>
  <div class="container">
    <ServerButton isHome />
    <div class="separator"></div>
    <ServerButton :mentions='3' />
    <ServerButton hasNotification />
    <ServerButton />
    <ServerButton hasNotification :mentions='5' />
    <ServerButton v-for="servers in 20" :key="servers.id" />
  </div>
</template>

<script>
import ServerButton from '../ServerButton'

export default {
  components: {
    ServerButton
  }
}
</script>

<style scoped lang="scss">
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
