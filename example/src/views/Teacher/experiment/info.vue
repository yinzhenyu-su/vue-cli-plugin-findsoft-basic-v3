<template lang="pug">
.main
  breadcrumb
  .div 这是详情页，主要用来展示面包屑
  div.pointer(@click="handleClick") 点击进入三级页面
</template>

<script lang="ts">
import { useRouter } from 'vue-router';
import { defineAsyncComponent, defineComponent } from 'vue';

export default defineComponent({
  components: {
    breadcrumb: defineAsyncComponent(() => import('@/components/Breadcrumbs.vue')),
  },
  props: {},
  setup() {
    const router = useRouter();
    return {
      handleClick() {
        router.push('/Teacher/experimentinfo/detail');
      },
    };
  },
});
</script>

<style lang="stylus" scoped>
.main
  .div
    margin 50px auto
</style>
