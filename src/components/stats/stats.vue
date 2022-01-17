<template>
<div class="stats">
  <div class="stats__border stats__right">
    <div class="stats__icon">
      <icon name="stars" />
      Star
    </div>
  </div>
    <div class="stats__border">
        {{stars}}
    </div>

     <div class="stats__border">
      <div class="stats__icon ">
        <icon name="forks" />
        Fork
      </div>
     </div>
      <div class="stats__border stats__left">
        {{forks}}
      </div>

    </div>

</template>

<script>
import { icon } from '../../icons'

export default {
  components: {
    icon
  },

  props: {
    stars: {
      type: Number,
      required: true
    },
    forks: {
      type: Number,
      required: true
    }
  },
  seturp () {
    return {}
  }
}
</script>
<style lang="scss">
.stats {
  display:flex;
  border-radius:14px;
  align-items: center;

  &__border {
    border:1px solid;
    padding:7px;
  }

  &__left {
    border-radius:0 4px 4px 0;
  }

  &__right {
    border-radius:4px 0 0 4px;
  }
}
</style>
