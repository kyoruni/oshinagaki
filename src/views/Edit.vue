<template>
  <div class="edit">
    <b-row>
      <div class="left col-8">
        <div class="preview m-4">
          <div class="preview__header" @click="clickHeader">
            <div class="preview__header__items">
              <div class="preview__header__items--event-date">
                {{ eventDate }}
              </div>
              <div class="preview__header__items--event-name">
                {{ eventName }}
              </div>
              <div class="preview__header__items--space-name">
                {{ spaceName }}
              </div>
              <div class="preview__header__items--circle-name">
                {{ circleName }}
              </div>
            </div>
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
          <editMenuHeader v-if="showMenuHeader"
            @eventDate="setEventDate"
            @eventName="setEventName"
            @spaceName="setSpaceName"
            @circleName="setCircleName"
            :eventDate="eventDate"
            :eventName="eventName"
            :spaceName="spaceName"
            :circleName="circleName"/>
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
      currentSection: 'default',
      eventDate: 'ddd',
      eventName: 'nnn',
      spaceName: 'sss',
      circleName: 'ccc'
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
    },
    setEventDate (value) {
      this.eventDate = value
    },
    setEventName (value) {
      this.eventName = value
    },
    setSpaceName (value) {
      this.spaceName = value
    },
    setCircleName (value) {
      this.circleName = value
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
    &__items {
      background: green;
      display: flex;
      width: 100%;
      height: 50px;
      margin-top: 25px;
      margin-bottom:25px;
      line-height: 50px;
      font-size: 36px;
      &--event-date {
        background: pink;
        width: 25%;
      }
      &--event-name {
        background: orange;
        width: 25%;
      }
      &--space-name {
        background: yellow;
        width: 25%;
      }
      &--circle-name {
        background: blue;
        width: 25%;
      }
    }
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