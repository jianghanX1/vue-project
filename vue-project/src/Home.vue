<template>
  <div>
    <Navigation></Navigation>
    <Content></Content>
    <Bottom></Bottom>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation';
import Content from '@/components/Content';
import Bottom from '@/components/Bottom';
export default {
  name: "Home",
  components: {
    Navigation,
    Content,
    Bottom
  }
}
</script>

<style scoped>

</style>
