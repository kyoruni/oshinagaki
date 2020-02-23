<template>
  <div class="home">
    <!-- インフォメーション -->
    <b-row class="mt-4">
      <div class="infomation col-8 mx-auto">
        <p class="text-center m-4">
          <span class="font-weight-bold">
            即売会向けお品書き画像作成サイト<br />
          </span>
          動作確認済：Chrome
        </p>
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
.infomation {
  background: #f98d6c;
  border-radius: 5px;
  color: #fff;
}
</style>