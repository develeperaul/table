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

      <MainNumber color="green" :text="item.title" mb="120"/>  
      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <div class="tw-relative">
        <MainNumber  color="red" text="-11111" mt="130" mb="75"/>  
        <img width="52px" height="109" v-if="index+1==json.length" class="arrow" src="../MainNumber/icons/up.svg" alt="">
      </div>

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <div class="tw-relative">
        <MainNumber  color="red" text="65489" mt="130" mb="75"/>   
        <img width="52px" height="109" v-if="index+1==json.length" class="arrow" src="../MainNumber/icons/down.svg" alt="">

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
 .arrow{
   position: absolute;
   top: 50%;
   right: -82px;
   
   
 }
</style>