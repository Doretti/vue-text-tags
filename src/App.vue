<template>
  <div class="wrapper">
    <div class="item item-big">
      <tag-list
        :tags="tags"
      />
    </div>
    <div class="item item-medium">
      <tag-list
        :tags="tags"
        align="left"
      />
    </div>
    <div class="item item-small">
      <tag-list
        :tags="tags"
      />
    </div>
  </div>
</template>

<script>
import TagList from './components/TagList.vue';
export default {
  name: 'App',

  components: {
    TagList
  },

  data: () => ({
    tags: [
      {
        value: 'На автобусе',
        icon: 'mdi-bus'
      },
      {
        value: 'На автобусе',
        icon: 'mdi-bus'
      },
      {
        value: 'На автобусе',
        icon: 'mdi-bus'
      },
      {
        value: 'На автобусе',
        icon: 'mdi-bus'
      },
      {
        value: 'На автобусе',
        icon: 'mdi-bus'
      },
      {
        value: '29 марта'
      },
      {
        value: '5',
        icon: 'mdi-star-outline'
      },
      {
        value: '6 часов',
        icon: 'mdi-clock'
      },
    ]
  }),
};
</script>

<style lang="scss">
  body {
    font-family: sans-serif;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  .item {
    height: 60px;
    background: #ccc;

    &-big {
      width: 80vw;
    }
    &-medium {
      width: 50vw;
    }
    &-small {
      width: 20vw;
    }
  }
</style>
