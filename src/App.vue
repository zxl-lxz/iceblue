<template>
  <div id="app">
    <ice-header></ice-header>
    <ice-first></ice-first>
    <ice-team></ice-team>
    <ice-ach></ice-ach>
    <ice-join></ice-join>
  </div>
</template>

<script>
import IceHeader from 'components/ice-header/ice-header'
import IceFirst from 'components/ice-first/ice-first'
import IceTeam from 'components/ice-team/ice-team'
import IceAch from 'components/ice-achievements/ice-ach'
import IceJoin from 'components/ice-join/ice-join'
export default {
  name: 'App',
  components: {
    IceHeader,
    IceFirst,
    IceTeam,
    IceAch,
    IceJoin
  }
}
</script>

<style lang="less" src="./index.less">
</style>
