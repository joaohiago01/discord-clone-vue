<template>
  <div id="grid">
    <ServerList />
    <ServerName />
    <ChannelList />
    <UserInfo />
  </div>
</template>

<script>
import ServerList from '../components/ServerList'
import ServerName from '../components/ServerName'
import ChannelList from '../components/ChannelList'
import UserInfo from '../components/UserInfo'

export default {
  components: {
    ServerList,
    ServerName,
    ChannelList,
    UserInfo
  }
}
</script>

<style scoped>
  #grid {
    display: grid;
    grid-template-columns: 71px 240px auto 240px;
    grid-template-rows: 46px auto 52px;
    grid-template-areas:
      "SL SN CI CI"
      "SL CL CD UL"
      "SL UI CD UL";
    height: 100vh;
  }
</style>
