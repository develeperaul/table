<template>
  <div class="tw-flex">
        <ColumnTable
      v-for="(item, index) in json"
      :key="index"
      v-bind="{index, item}"
    > 
      <span
        class="date">
        {{item.date}}
      <BorderLine
      style="margin-top: 25px"
      :style="{marginLeft:[index>0 ? '-30px': '']}"/>
      </span>

      <MainNumber color="red" text="110,4%" mb="35" after="план"/>  
      <MainNumber color="green" text="111,4%" mb="35" execution="failed" after="факт"/>  

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Величина среднедушевого денежного дохода"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
        <MainNumber  color="red" :text="item.title" mt="130" mb="75" />  

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
        },
        {
          date: 2018,
          title: '72,06Р',
        },
        {
          date: 2018,
          title: '72,08Р',
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
 .people{
   position: absolute;
   top: 50%;
   right: -82px;
   transform: translateY(-25%);
   
 }
</style>
</script>
