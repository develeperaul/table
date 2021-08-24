<template>
  <div>
    <MainNumber text="94,9%" color="green" fs="300" lh="300"/>
    <div class="tw-flex">
      <ColumnTable
        v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length }"
      >
          <span
          class="date">
            {{item.date}}  
          
          <TableGradientLine 
            colorGradient ="green" 
            text="Среднедушевой денежный доход населения за отчетный год"
            :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
          </span>
          <MainNumber :text="item.numb1"/>

          <TableGradientLine 
            colorGradient ="green" 
            text="Среднемесячная начисленная заработная плата"
            :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
          
          <MainNumber :text="item.numb2" color="orange"/>
      </ColumnTable>
    </div>
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import TableGradientLine from "components/TableGradientLine";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber,
    TableGradientLine
  },
  data () {
    return {json: [
      {
        date: 2019,
        numb1: "30517,5Р",
      },
      {
        date: 2020,
        numb1: "30035Р",
        numb2: "38706Р"
      },
      {
        date: 2021,
        numb2: "30517,5Р"
      }
    ]}
  }
}
</script>
