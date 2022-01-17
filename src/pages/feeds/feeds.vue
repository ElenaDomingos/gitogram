<template>
<div class="topline">

  <topline>
    <template #headline>
      <div class="headline">
        <div class="headline__container">
          <h1>Gitogram /</h1>
            <div class="icons">

              <span class="icon">
                <icon name="home"/>
              </span>
              <span class="icon">
                <icon name="avatar" />
              </span>
              <span class="icon">
                <icon name="exit" />
              </span>

            </div>
          </div>

            <ul class="users">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item
            :avatar="story.avatar"
            :username="story.username"
            @onPress="handlePress(story.id)"/>

          </li>

        </ul>

      </div>
    </template>
    <template #content>
      <div class="container">

        <ul class="posts__list">
          <li v-for="item,ndx in 5" :key="ndx" class="posts__item">
            <feed>
              <template #card><card /></template>
            </feed>
          </li>
        </ul>
      </div>
    </template>
  </topline>
</div>

</template>
<script>

import { topline } from '../../components/topline'
import { icon } from '../../icons'
import { storyUserItem } from '../../components/storyUserItem'
import stories from './data.json'
import { feed } from '../../components/feed'
import { card } from '../../components/card'

export default {
  name: 'feeds',
  components: {

    topline,
    icon,
    storyUserItem,
    feed,
    card

  },
  data () {
    return {
      stories
    }
  }
}
</script>
<style lang="scss">
.headline {
  padding-left:52px;

  &__container {
    width:1280px;
    margin:0 auto;
    display:flex;
    justify-content: space-between;
  }
}

.container {
   width:1280px;
    margin:0 auto;
}

.users {
  display:flex;
  justify-content: flex-start;

}

.stories-item {
  margin-right:50px;
}
</style>
