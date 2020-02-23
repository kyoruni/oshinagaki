<template>
  <div id="app">
    <font-awesome-icon :icon="['fas', 'user-secret']" />
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">お品書きメーカー</b-navbar-brand>
    </b-navbar>
    <router-view/>
  </div>
</template>
