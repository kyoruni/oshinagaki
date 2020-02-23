<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand to="/">
        <font-awesome-icon icon="pen" />
        お品書きメーカー
        </b-navbar-brand>
    </b-navbar>
    <b-container fluid>
      <b-row>
        <router-view/>
      </b-row>
    </b-container>
  </div>
</template>
