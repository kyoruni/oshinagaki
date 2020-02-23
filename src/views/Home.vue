<template>
  <div class="home">
    <!-- インフォメーション -->
    <b-row class="mt-4">
      <div class="infomation col-8 mx-auto">
        <div class="text-center m-4">
          <p class="infomation--title">
            即売会向けお品書き画像作成ツール<br />
          </p>
          <span class="infomation--operation-check">
            動作確認済：Chrome
          </span>
        </div>
      </div>
    </b-row>
    <!-- お知らせ -->
    <news />
    <!-- 作る！ -->
    <div class="making mt-4">
      <button class="making--button p-3">
        作る！
      </button>
    </div>
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
  // 動作確認
  &--operation-check {
    font-size: 0.8rem;
  }
}

// 作る！
.making {
  text-align: center;
  // ボタン
  &--button {
    background: #82d02f;
    border: 1px solid #82d02f;
    border-radius: 5px;
    color: #fff;
    font-weight: bold;
    opacity: 0.7;
    transition: 0.3s ease-in-out;
    width: 150px;
    -webkit-transition: 0.3s ease-in-out;
    // ボタンにマウス乗せたとき
    &:hover {
      opacity: 1.5;
    }
  }
}
</style>
