<template>
  <div>
    <Navigation></Navigation>
    <router-view></router-view>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation';
export default {
  name: "Home",
  components: {
    Navigation
  },
  data() {
    return {

    }
  }
}
</script>

<style lang="less" scoped>

</style>
