<template>
  <div class="tw-flex">
    <ColumnTable
            v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length}"
        pb="120">
        <span
        class="date">
          {{item.date}}
        
        </span>
        <TableGradientLine 
          colorGradient ="green" 
          text="Без учета жилых домов, построенных на земельных участках, предназначенных для ведения гражданами садоводства"
          :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
        
        
          <MainNumber  :text="item.numb1" color="green" mb="60"
          fs="200" lh="200"
          />
        <!-- <div class="tw-w-full tw-relative "> -->
          <TableGradientLine 
            colorGradient ="green" 
            text="Ввод общей площади жилых домов, построенных населением"
            :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
        <!-- </div> -->
        <MainNumber :text="item.numb2" mt="50" color="green"/>
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
          numb1: "0.9",
        },
        {
          date: 2019,
          numb1: "1",
          numb2: "3.455"
        },
        {
          date: 2020,
          numb1: "1",
          numb2: "3.681"
        }
      ]
    }
  }
}
</script>
