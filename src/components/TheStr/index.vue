<template>
  <div class="tw-flex">
    <ColumnTable
            v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length}">
        <span
        class="date">
          {{item.date}}
          <BorderLine
          style="margin-top: 25px"
          :style="{marginLeft:[index>0 ? '-30px': '']}"/>
        </span>
        <template>
          <MainNumber :text="item.numb1" :after="item.numb2? 'план' : true" mb="60"/>
          <MainNumber  :text="item.numb2" after="факт" color="green" execution="completed" mb="60"
          :style="{opacity: item.numb2 ? 1 : 0}"/>
        </template>
        <!-- <div class="tw-w-full tw-relative "> -->
          <TableGradientLine 
            colorGradient ="green" 
            text="Без учета жилых домов, построенных на земельных участках, предназначенных для ведения гражданами садоводства"
            :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
        <!-- </div> -->
        <MainNumber :text="item.numb3" mt="50"/>
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
    return {json: [
      {
        date: 2018,
        numb1: "2,29",
        
      },
      {
        date: 2018,
        numb1: "2,29",
        numb3: "2,29",
      },
      {
        date: 2018,
        numb1: "2,29",
        numb2: "2,29",
        numb3: "2,29",
      },
      {
        date: 2018,
        numb1: "2,29",
      },
      {
        date: 2018,
        numb1: "2,29",
      },
    ]}
  }
}
</script>
