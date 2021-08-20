<template>
<!-- колонна таблицы -->
    <div

      class="tw-flex tw-flex-col "
      :class="`tw-w-1/${length}`"
      :style="[{background:(index+1)%2==0 ? ' rgba(196, 196, 196, 0.05)' : ''}, {paddingLeft:index>0 ? `${pl}px`: ''}, {paddingBottom: `${pb}px`}]"
      
    >
    
    <slot></slot>

    </div>
</template>

<script>
export default {
  props: {
    index: {
      type: Number,
      required: true,
    },
    item: {
      type: Object,
      required: true,
    },
    length: {
      type: Number,
      required: true
    },
    pb: {
      type: String,
      required: false,
      default: "55"
    },
    pl: {
      type: String,
      required: false,
      default: "30"
    },
  },
  // name: 'ComponentName',
  data () {
    return {}
  }
}
</script>
