<template>
<!-- колонна таблицы -->
    <div

      class="tw-flex tw-flex-col "
      :class="`tw-w-1/3`"
      :style="[{background:(index+1)%2==0 ? ' rgba(196, 196, 196, 0.05)' : ''}, {paddingLeft:index>0 ? '30px': ''}, {paddingBottom: `${pb}px`}]"
      
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
    pb: {
      type: String,
      require: false,
      default: "55"
    }
  },
  // name: 'ComponentName',
  data () {
    return {}
  }
}
</script>
