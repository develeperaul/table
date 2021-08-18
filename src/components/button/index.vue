<template>
          <img 
          v-if="icon"
          class="tw-inline-block tw-align-baseline"
          width="77px"
          height="77px"
          :src="require('./icons/' + icon + '.svg')">
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: false
    }
  },
  // name: 'ComponentName',
  data () {
    return {}
  }
}
</script>
