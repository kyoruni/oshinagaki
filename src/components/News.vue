<template>
  <div class="news">
    <b-row class="mt-4">
      <div class="main col-8 mx-auto">
        <ul class="m-2">
          <li v-for="news in newsList" :key="news.id" class="news-list">
            <font-awesome-icon icon="rss" class="news-list--icon" />
            <span class="news-list--date">
              {{ news.date }}
            </span>
            <span class="news-list--title">
              {{ news.title }}
            </span>
          </li>
        </ul>
      </div>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'News',
  data () {
    return {
      newsList: [
        { id: 1, date: '2020-01-23', title: 'お知らせ1' },
        { id: 2, date: '2020-01-23', title: 'お知らせ2' },
        { id: 3, date: '2020-01-24', title: 'お知らせ3' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.main {
  color: #6c757d;
}

ul {
  list-style: none;
}

li {
  margin-bottom: 5px;
}

// お知らせリスト
.news-list {
  color: #3d3d3d;
  height: 25px;
  line-height: 25px;
  // お知らせリストのアイコン
  &--icon {
    margin-right: 4px;
  }
  // お知らせリストの日付
  &--date {
    color: #7f7f7f;
    font-size: 0.8rem;
  }
}
</style>