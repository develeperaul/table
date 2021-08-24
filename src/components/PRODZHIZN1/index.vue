<template>
  <div class="tw-flex">
        <ColumnTable
      v-for="(item, index) in json"
      :key="index"
      v-bind="{index, item, length: json.length }"
    > 
      <span
        class="date">
        {{item.date}}
      <BorderLine
      style="margin-top: 25px"
      :style="{marginLeft:[index>0 ? '-30px': '']}"/>
      </span>

      <MainNumber color="green" text="72,64" mb="35" after="план"/>  
      <MainNumber color="green" text="72,64" mb="35" execution="failed" after="факт"/>  

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Мужчины"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <div class="tw-relative">
        <MainNumber  color="red" text="-11111" mt="130" mb="75"/>  
        <img width="52px" height="109" v-if="index+1==json.length" class="people" src="../MainNumber/icons/man.svg" alt="">
      </div>

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Женщины"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <div class="tw-relative">
        <MainNumber  color="red" text="65489" mt="130" mb="75"/>   
        <img width="52px" height="109" v-if="index+1==json.length" class="people" src="../MainNumber/icons/woman.svg" alt="">

      </div>
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
          title: 4051005,
        },
        {
          date: 2018,
          title: 4051005,
        },
        {
          date: 2018,
          title: 4051005,
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
