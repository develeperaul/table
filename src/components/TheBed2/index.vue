<template>
  <div>
    <div class="tw-flex tw-justify-between"
    style="margin-bottom: 230px">
      <div>
        <span class="title">
          Номинальная заработанная плата на декабрь 2020г.
        </span>
        <MainNumber text="38706Р" fs="220" lh="220" color="green" trend="bigdown"/>
      </div>
      <div>
        <span class="title">
          Номинальная заработанная плата на февраль 2021г. 
        </span>
        <MainNumber text="37448Р" fs="220" lh="220" color="orange" trend="bigdown"/>
      </div>
    </div>
      <TableGradientLine colorGradient="green"
      text=" Величина прожиточного минимума в субъекте Российской Федерации 
  (в РБ на душу населения в среднем за месяц, в руб.)"/>
    <div class="tw-flex">
          <ColumnTable
        v-for="(item, index) in json"
        :key="index"
        v-bind="{index, item, length: json.length }"
        class="tw-flex tw-flex-col tw-justify-between"
      > 
      <span class="date">
        {{item.date}}
      </span>
      
      <MainNumber :text="item.title"/>

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
          title: '72,06Р',
        },
        {
          date: 2018,
          title: '72,06Р',
        },
        {
          date: 2018,
          title: '72,08Р',
        },
        {
          date: 2018,
          title: '72,06Р',
        },
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
  .title {
    font-size: 50px;
    line-height: 68.09px;
    font-weight: 700;
    display: block;
    max-width: 70%;
    margin-bottom: 45px;
  }
  .date {
    margin-bottom: 45pxf;
    margin-top: 70px;
  }
</style>

