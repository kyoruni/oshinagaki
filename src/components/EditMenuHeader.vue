<template>
  <div class="edit-menu-header">
    <!-- 日付 -->
    <div class="form-group">
      <label for="inputEventDate">イベント開催日</label>
      <input
        type="text"
        class="form-control"
        id="inputEventDate"
        placeholder="イベント開催日"
        :value="eventDate"
        @input="setEventDate">
    </div>
    <!-- イベント名 -->
    <div class="form-group">
      <label for="inputEventName">イベント名</label>
      <input type="text" class="form-control" id="inputEventName" placeholder="イベント名">
    </div>
    <!-- スペース名 -->
    <div class="form-group">
      <label for="inputSpaceName">スペース名</label>
      <input type="text" class="form-control" id="inputSpaceName" placeholder="スペース名">
    </div>
    <!-- サークル名 -->
    <div class="form-group">
      <label for="inputCircleName">サークル名</label>
      <input type="text" class="form-control" id="inputCircleName" placeholder="サークル名">
    </div>
  </div>
</template>

<script>
export default {
  name: 'EditMenuHeader',
  methods: {
    setEventDate (value) {
      this.$emit('eventDate', value.target.value)
    }
  },
  props: [
    'eventDate'
  ]
}
</script>