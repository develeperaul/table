<template>
<!-- таблица NAS1 -->
  <div
  class="tw-flex">
  
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

      <MainNumber color="green" text="46541651" mb="120"/>  

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <MainNumber class="main-number--pos" color="red" text="-11111" mt="130" mb="75"/>  

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <MainNumber class="main-number--pos" color="red" text="65489" mt="130" mb="75">   
            <template
              slot="before"
              >
              к = 11,6
            </template>
      </MainNumber>

      <!-- </div> completed failed-->
    </ColumnTable>

  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import BorderLine from "components/BorderLine";
import TableGradientLine from "components/TableGradientLine"
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
  .date {
    font-size: 50px;
    font-weight: 700;
    line-height: 68.09px;
    margin-bottom: 75px;
    
    margin-top: 21px;
  }
  .main-number--pos{
    margin-top: 95px;
  }
</style>
