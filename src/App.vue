<template>
  <div id="app">
    <ice-header></ice-header>
    <ice-team></ice-team>
    <ice-ach></ice-ach>
    <ice-join></ice-join>
  </div>
</template>

<script>
import IceHeader from 'components/ice-header/ice-header'
import IceTeam from 'components/ice-team/ice-team'
import IceAch from 'components/ice-achievements/ice-ach'
import IceJoin from 'components/ice-join/ice-join'
export default {
  name: 'App',
  components: {
    IceHeader,
    IceTeam,
    IceAch,
    IceJoin
  }
}
</script>

<style>
  @import 'assets/reset.css';
  html,
  body {
    height: 100%;
  }
  #app {
    height: 100%;
  }
</style>
