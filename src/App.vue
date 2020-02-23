<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" class="header-nav">
      <b-navbar-brand to="/">
        <font-awesome-icon icon="pen" />
        お品書きメーカー
        </b-navbar-brand>
    </b-navbar>
    <b-container fluid>
      <router-view/>
    </b-container>
  </div>
</template>

<style lang="scss" scoped>
.header-nav {
  background: #f98d6c;
}
</style>
