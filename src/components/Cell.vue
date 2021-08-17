<template>
<!-- ячейка -->
  <div>
    <CellNumber v-bind="{item, indexCol: index}"/>
  </div>
</template>

<script>
import CellNumber from "components/CellNumber"

export default {
  props: {
    item: {
      required: true,
      type: Object
    },
    index: {
      required: true,
      type: Number
    },

  },
  // name: 'ComponentName',
  components: {
    CellNumber

  },
  data () {
    return {
      json: [
        {
          title: 'суммарный коэффициент рождаемости',
          subtitle: '1,652'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>


</style>
