<template>
  <div class="tw-flex">
    <ColumnTable
    v-for="(item, index) in json"
    :key="index"
    v-bind="{index, item, length: json.length}"
    pb="33">
      <span
        class="date">
          {{item.date}}
          <BorderLine
          style="margin-top: 25px"
          :style="{marginLeft:[index>0 ? '-30px': '']}"/>
      </span>
      <MainNumber :text="item.numb1" color="green" fs="200" lh="200"/>
      <TableGradientLine 
        colorGradient ="green" 
        text="Доля городов Республики Башкортостан с благоприятной городской средой"
        :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
      <template>
        <MainNumber :text="item.numb2" :after="item.numb2? 'план' : true" mb="60"/>
        <MainNumber  :text="item.numb3" after="факт" color="green" execution="completed" mb="60"
        :style="{opacity: item.numb3 ? 1 : 0}"/>
      </template>
      <TableGradientLine 
        colorGradient ="green" 
        text="Индекс качества городской среды по субъекту Российской Федерации за отчетный год "
        :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
      <MainNumber  :text="item.numb4" mb="60"/>

    </ColumnTable>
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import BorderLine from "components/BorderLine";
import TableGradientLine from "components/TableGradientLine";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber, 
    BorderLine,
    TableGradientLine
  },
  data () {
    return {
      json: [
        {
          date: 2018,
          numb1: '172',
          numb4: "163"
        },
        {
          date: 2019,
          numb1: "176",
          numb2: "33%",
          numb3: "33%",
          numb4: "169"
        },
        {
          date: 2020,
          numb1: "184",
          numb2: "38%",
          numb3: "43%"
        }
      ]
    }
  }
}
</script>
