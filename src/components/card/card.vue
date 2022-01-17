<template>
<div class="card">
  <div class="card__title_wrap">
    <h2 class="card__title">Title</h2>
  </div>
  <div class="card__description">JavaScript framework for building interactive web applications ⚡</div>
  <div class="card__stats">
    <stats :stars="10" :forks="5" />
  </div>
</div>
</template>

<script>
import { stats } from '../../components/stats'

export default {
  components: {
    stats
  }
}
</script>

<style lang="scss" scoped>
.card {
  background: #FFFFFF;
border: 1px solid #F1F1F1;
box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.07);
border-radius: 10px;
text-align: left;
padding:24px 20px;
margin-top:16px;

&__description {
margin-bottom:12px;
}
}
</style>
