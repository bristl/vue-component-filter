<template lang='pug'>
  .wrapper
    button(
      v-for="tab in tabs"
      v-bind:key="tab"
      v-bind:class="['tab-button', { active: currentTab === tab }]"
      v-on:click="currentTab = tab"
    ) {{ tab.name }}

    keep-alive
      component(
        v-bind:is="currentTab.component"
        class="tab"
      )
</template>

<script>
import tinkoff from './Tabs/tinkoff'
import games from './Tabs/games'
var tabs = [
  {
    name: 'tinkoff',
    component: tinkoff
  },
  {
    name: 'games',
    component: games
  }
]

export default {
  name: 'Home',
  data () {
    return {
      tabs: tabs,
      currentTab: tabs[0]
    }
  }
}
</script>
.tab-button {
  padding: 6px 10px;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
  border: 1px solid #ccc;
  cursor: pointer;
  background: #f0f0f0;
  margin-bottom: -1px;
  margin-right: -1px;
}
.tab-button:hover {
  background: #e0e0e0;
}
.tab-button.active {
  background: #e0e0e0;
}
.tab {
  border: 1px solid #ccc;
  padding: 10px;
}
<style lang='stylus'>
</style>
