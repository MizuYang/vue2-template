<template>
  <div class="btn btn-mizuTest">按鈕</div>
</template>

<script>
export default {
  mounted () {
    this.$http.get('https://randomuser.me/api/')
      .then(res => {
        console.log(res)
        this.isLoading = false
      })
      .catch(err => {
        console.log(err)
      })
  }
}
</script>

<style scoped lang="scss">
</style>
