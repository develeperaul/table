<template>
  <div class="tw-flex">
    
      <ColumnTable
        v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length }">
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
        

        <span
        class="date"
        style="margin-bottom: 0px">
          <BorderLine
          
          :style="{marginLeft:[index>0 ? '-30px': '']}"/>
          {{item.date}}
        </span>
      </ColumnTable>
    
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber  from "components/MainNumber";
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
      json : [
        {
          date: 2018,
          numb1: "110,74",
          
        },
        {
          date: 2019,
          numb1: "113,04",
          numb2: "110,74"
        },
        {
          date: 2020,
          numb1: "225,87",
          numb2: "110,74"
        }
      ]
    }
  }
}
</script>
