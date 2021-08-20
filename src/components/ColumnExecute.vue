<template>
  <ColumnTable>
    <MainNumber after="план"/>
    <MainNumber after="факт"/>
  </ColumnTable>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber  from "components/MainNumber";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber
  },
  data () {
    return {}
  }
}
</script>
