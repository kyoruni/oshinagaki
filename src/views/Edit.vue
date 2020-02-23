<template>
  <div class="edit">
    <b-row>
      <div class="left col-8">
        <div class="preview m-4">
          preview
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
  border: 1px solid #333;
  height: 800px;
}
</style>