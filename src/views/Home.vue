<template>
  <div class="home">
    <!-- インフォメーション -->
    <b-row class="mt-4">
      <div class="infomation col-8 mx-auto">
        <div class="text-center m-4">
          <p class="infomation--title">
            即売会向けお品書き画像作成サイト<br />
          </p>
          <span class="infomation--operation-check">
            動作確認済：Chrome
          </span>
        </div>
      </div>
    </b-row>
    <!-- お知らせ -->
    <news />
  </div>
</template>

<script>
import news from '../components/News'

export default {
  name: 'Home',
  components: {
    news
  }
}
</script>

<style lang="scss" scoped>
// インフォメーション
.infomation {
  background: #f98d6c;
  border-radius: 5px;
  color: #fff;
  // インフォメーションのタイトル
  &--title {
    font-weight: bold;
    margin-bottom: 6px;
  }
}
</style>