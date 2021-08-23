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
        </span>
        <TableGradientLine 
          colorGradient ="green" 
          text="Число работников юридических лиц"
          :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />
          <MainNumber color="green" :text="item.numb1" mt="41" mb="65" />
          <Cell v-bind="{item: item.info, index}"/>
          <TableGradientLine 
          colorGradient ="green" 
          text="Число индивидуальных предпринимателей"
          :style="{width: `${100*json.length}%`, opacity: index>0 ? '0' : '1'}" />  
          <MainNumber color="green" :text="item.numb2"  mt="41" mb="55"/>
          <Cell v-bind="{item: item.info2, index}"/>
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
          numb1: '884,7 ',
          numb2: '243,33 ',
          info: [
            {
              title: 'Число работников средних предприятий',
              subtitle: '61,312'
            },
            {
              title: 'Число работников малых предприятий',
              subtitle: '95,297 '
            },
            {
              title: 'Число работников микропредприятий предприятий',
              subtitle: '413,363'
            },
            {
              title: 'летучие органические ',
              subtitle: '173,247 '
            }
          ],
          info2: [
            {
              title: 'Число работников индивидуальных предпринимателей',
              subtitle: '135,144'
            },
          ]
        },
        {
          date: '2019',
          numb1: '597,5',
          numb2: '236,02',
          info: [
            {
              subtitle: '60,325'
            },
            {
              subtitle: '68,111'
            },
            {
              subtitle: '171,636'
            },
            {
              subtitle: '140,242'
            },

          ],
          info2: [
            {
              subtitle: '135,144'
            },
          ]
        },
        {
          date: '2020',
          numb1: '559,307',
          numb2: '209,77',
          info: [
            {
              subtitle: '59,046'
            },
            {
              subtitle: '65,73'
            },
            {
              subtitle: '166,265 '
            },
            {
              subtitle: '135,144'
            },
          ],
          info2: [
            {
              subtitle: '135,144'
            },
          ]
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