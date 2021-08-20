<template>
  <div>
    <span class="text">
      Объем инвестиций в основной капитал по всем хозяйствующим субъектам с учетом оценки объема инвестиций, не наблюдаемых прямыми статистическими методами за отчетный год,  млрд.руб. (на 4 квартал 2020)
    </span>
    <MainNumber text="365,9" color="green" mt="32" mb="62" fs="300" lh="300"/>
    <span class="text">Темп роста (индекс роста) физического объема инвестиций в основной капитал, за исключением инвестиций инфраструктурных монополий (федеральные проекты) и бюджетных ассигнований федерального бюджета, %</span>

    <div class="tw-flex">
      <ColumnTable
      v-for="(item, index) in json"
      :key="index"
      v-bind="{index, item, length: json.length, reverse: true }"
      >
        <span
        class="date"
        style="margin-bottom: 50px">
          {{item.date}}
          <BorderLine
          style="margin-top: 25px"
          :style="{marginLeft:[index>0 ? '-30px': '']}"/>
          <MainNumber :text="item.numb1" after="план"/>
          <MainNumber :text="item.numb2" after="факт" color="green"  />
          
        </span>
      </ColumnTable>
    </div>
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import TableGradientLine from "components/TableGradientLine";
import BorderLine from "components/BorderLine";
// import BorderLine from "components/BorderLine";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber,
    TableGradientLine,
    BorderLine
  },
  data () {
    return {
      json: [
        {
          date: 2019,
          numb1: "104,9%",
          numb2: "111,7%"
        },
        {
          date: 2020,
          numb1: "110,1%",
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
  }
</style>
