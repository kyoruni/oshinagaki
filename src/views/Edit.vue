<template>
  <div class="edit">
    <b-row>
      <div class="left col-8">
        <div class="preview m-4">
          <div class="preview__header">
            header
          </div>
          <div class="preview__body">
            body
          </div>
        </div>
      </div>
      <div class="right col-4">
        right
      </div>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'Edit'
}
</script>

<style lang="scss" scoped>
.preview {
  background: pink;
  height: 600px;
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
</style>