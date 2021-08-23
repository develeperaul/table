<template>
  <div>
    <span class="text">
      Численность занятых в сфере малого и среднего предпринимательства, включая индивидуальных предпринимателей и самозанятых, тыс.чел.
    </span>
    <div class="tw-flex">
          <ColumnTable
        v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length, reverse: true }"
      > 
        <span
          class="date">
          {{item.date}}
        <BorderLine
        style="margin-top: 25px"
        :style="{marginLeft:[index>0 ? '-30px': '']}"/>
        </span>

        <MainNumber color="red" text="110,4%" mb="35" after="план"/>  
        <MainNumber color="green" text="111,4%" mb="70" execution="completed" after="факт"/>  

        <div class="tw-w-full tw-relative">
          <TableGradientLine v-if="index<1" colorGradient="green"
          text="По методике расчета показателя Указа № 193"
          class="tw-absolute"
        :style="{width: `${100*json.length}%`}" 
          />
        </div>
          <MainNumber  color="red" :text="item.title" mt="130" mb="75" execution="failed"/>  

      </ColumnTable>

    </div>

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
          title: '72,06%',
        },
        {
          date: 2018,
          title: '72,06%',
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
  .text {
    font-size: 50px;
    line-height: 50px;
    display: inline-block;
    margin-bottom: 66px;
  }
</style>
