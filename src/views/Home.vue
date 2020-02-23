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
    <!-- 説明書き -->
    <b-row>
      <div class="description col-8 mt-4 mx-auto">
        <ul class="m-4">
          <li>即売会参加告知用のお品書き画像が、ブラウザ上で簡単に作成できます。</li>
          <li>頑張って作成中！</li>
        </ul>
      </div>
    </b-row>
    <!-- 注意書き -->
    <div class="notes fixed-bottom p-4">
      <ul class="mx-auto col-8">
        <li>使用する環境によっては正しく動作しない場合があります。</li>
        <li>作成した画像の再配布は禁止です。</li>
        <li>印刷用の解像度ではないため、ポスター等の使用はできません。</li>
        <li>使用報告、クレジット記載は不要です。</li>
      </ul>
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

// 説明書き
.description {
  font-size: 0.9rem;
  li {
    margin-bottom: 10px;
    &:last-child {
      margin-bottom: 0;
    }
  }
}

// 注意書き
.notes {
  background: #3d3d3d;
  color: #fff;
  ul {
    font-size: 0.8rem;
  }
  li {
    margin-bottom: 10px;
    &:last-child {
      margin-bottom: 0;
    }
  }
}
</style>
