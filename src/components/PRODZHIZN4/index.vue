<template>
<!-- таблица NAS5 PROD_ZHIZN4 NAS4 PROD_ZHIZN3-->
    <div class="tw-flex tw-w-full tw-relative">
      <TableGradientLine 
      colorGradient="green"
      class="tw-absolute"
      style="top: 95px;"
      text="Число родившихся (в т.ч. на 1000 человек населения) "/>
      
      <ColumnTable 
      v-for="(item, index) in json"
      :key="index"
      v-bind="{index, item, length: json.length }"
      pb="135"
      >
        <span
          class="tw-text-xl date"
          style="margin-bottom: 20px"
        >2018</span>
        <div class="tw-flex tw-flex-col">
          <MainNumber color="green" text="47010" mt="80" mb="50" before="к = 11,6"
          />
            <Cell v-bind="{item: item.info, index, endLine: true}"/>
            
        </div>
        <!-- {{'261(10231)'.search(/[(]/)}} -->
      </ColumnTable>
    </div>
    


</template>

<script>
import Cell from "components/Cell";
import TableGradientLine from "components/TableGradientLine";
import MainNumber from "components/MainNumber"

import ColumnTable from "components/ColumnTable"
export default {
  components : {
    ColumnTable,

    Cell,
    TableGradientLine,
    MainNumber
  },
  // name: 'ComponentName',

  data () {
    return {
      json: [
        {
          date: '2018',
          title: '47010',
          koef: 'к = 11,6',
          info: [
            {
              title: 'суммарный коэффициент рождаемости',
              subtitle: '1,652'
            },
            {
              title: 'численность женщин в репродуктивном возрасте (15-49 лет)',
              subtitle: '934 198'
            },
            {
              title: 'средний возраст матери при рождении первенца',
              subtitle: '26'
            },
            {
              title: 'коэффициент брачности/разводимости',
              subtitle: '6,3/3,8'
            },
            {
              title: 'младенческая смертность (в т.ч. на 1000 человек населения)',
              subtitle: '240 (к. 5,1)'
            }
          ],
        },
        {
          date: '2018',
          title: '47010',
          koef: 'к = 11,6',
          info: [
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '240 (к. 5,1)'
            },
          ],
        },
        {
          date: '2018',
          title: '47010',
          koef: 'к = 11,6',
          info: [
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '1,511'
            },
            {
              subtitle: '240 (к. 5,1)'
            },
          ],
        },
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
    margin-bottom: 40px;
    margin-top: 21px;
  }


  .text-gradient {
    font-size: 40px;
    line-height: 54.47px;
    font-weight: 400;
    margin-left: 20px;
    white-space: nowrap;
  }
</style>