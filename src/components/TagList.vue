<template>
  <div :class="'tag-list__wrapper' + (align === 'left' ? ' tag-list__wrapper-left' : '')">
    <div v-for="(item, index) of tags" :key="index" class="tag-list__item">
        <v-icon class="tag-list__divider" small v-if="index">
            mdi-circle-medium
        </v-icon>
        <v-icon small v-if="item.icon">
            {{item.icon}}
        </v-icon>
        {{item.value}}
    </div>
  </div>
</template>

<script>
export default {
    props: {
        tags: {
            type: Array
        },
        align: {
            type: String
        }
    },
    methods: {
        isHidden(ref) {
            console.log(this.$refs);
        }
    }
}
</script>

<style lang="scss">
.tag-list {
    &__wrapper {
        padding: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        width: 100%;
        position: relative;
        overflow: hidden;
        height: 20px;
    }
    &__wrapper-left {
        justify-content: flex-start;
    }
    &__item {
        font-size: 14px;
        color: #262626;
        display: flex;
        align-items: center;
        justify-content: space-between;
        column-gap: 3px;
        position: relative;
        word-break: keep-all;
        white-space: nowrap;
    }
    &__divider {
        margin-left: 3px;
    }
}
</style>