<template>
  <div class="tw-flex">
    
    <ColumnTable
        v-for="(item, index) in json"
    :key="index"
    v-bind="{index, item, length: json.length}">
      <span
        class="date"
        style="margin-bottom: 50px">
          {{item.date}}
          <BorderLine
          style="margin-top: 25px"
          :style="{marginLeft:[index>0 ? '-30px': '']}"/>
      </span>
      <MainNumber :text="item.numb1" after="план" fs="150" lh="150" mb="50"/>
      <MainNumber :text="item.numb2" after="факт" fs="150" lh="150" color="green"/>
    </ColumnTable>
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import BorderLine from "components/BorderLine";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber,
    BorderLine
  },
  data () {
    return {
      json: [
        {
          date: 2018,
          numb1: "100%",
          numb2: "108,38%"
        },
        {
          date: 2019,
          numb1: "100,04%",
          numb2: "105,95%"
        }
      ]
    }
  }
}
</script>
