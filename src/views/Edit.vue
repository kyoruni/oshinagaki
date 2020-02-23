<template>
  <div class="edit">
    <b-row>
      <div class="left col-8">
        <div class="preview m-4">
          <div class="preview__header" @click="clickHeader">
            header
          </div>
          <div class="preview__body" @click="clickBody">
            body
          </div>
        </div>
      </div>
      <div class="right col-4">
        <div class="menu mt-4">
          <div class="menu__default" v-if="showDefault">
            default
          </div>
          <editMenuHeader v-if="showMenuHeader" />
          <editMenuBody v-if="showMenuBody" />
        </div>
      </div>
    </b-row>
  </div>
</template>

<script>
import EditMenuHeader from '../components/EditMenuHeader';
import EditMenuBody from '../components/EditMenuBody';

export default {
  name: 'Edit',
  data () {
    return {
      currentSection: 'default'
    }
  },
  components: {
    EditMenuHeader,
    EditMenuBody
  },
  methods: {
    clickHeader () {
      this.currentSection = 'header';
    },
    clickBody () {
      this.currentSection = 'body';
    }
  },
  computed: {
    showDefault () {
      return this.currentSection === 'default';
    },
    showMenuHeader () {
      return this.currentSection === 'header';
    },
    showMenuBody () {
      return this.currentSection === 'body';
    }
  }
}
</script>

<style lang="scss" scoped>
.preview {
  background: pink;
  &__header {
    background: lime;
    border: 1px solid #333;
    height: 100px;
  }
  &__body {
    background: aqua;
    border: 1px solid #333;
    border-top: none;
    height: 500px;
  }
}

.menu {
  background: yellow;
}
</style>