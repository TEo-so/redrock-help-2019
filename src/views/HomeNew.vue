<template>
  <div class="home-new">
    <div class="question">
      <VQuestion
        :isLoading="isLoading"
        :questionData="questionList"
      />
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import { FETCH_QUESTION_NEW } from '@/store/type/actions'

export default {
  name: 'homeNew',
  mounted () {
    this.$store.dispatch(FETCH_QUESTION_NEW)
  },
  computed: {
    ...mapGetters(['isLoading', 'questionList']),
  },
}
</script>

<style lang="less" scoped>
.home-new {
  margin-top: 30px;
}
</style>

