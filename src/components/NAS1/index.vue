<template>
<!-- таблица NAS1 -->
  <div
  class="tw-flex">
  
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

      <MainNumber color="green" :text="item.title" mb="120"/>  

      <div>
        <div class="tw-w-full tw-relative">
          <TableGradientLine v-if="index<1" colorGradient="green"
          text="Миграционный прирост"
          class="tw-absolute"
        :style="{width: `${100*json.length}%`}" 
          />
        </div>
        <div class="tw-relative">
          <MainNumber
            color="red"
            text="-8858"
            mt="130"
            mb="75"
            />
          <Button v-if="index+1==json.length" icon="next" class="tw-absolute tw-top-0 tw-right-0 tw-transform tw-translate-y-1/3"/>
        </div>
      </div>

      <div>
        <div class="tw-w-full tw-relative">
          <TableGradientLine v-if="index<1" colorGradient="green"
          text="Естественный прирост"
          class="tw-absolute"
        :style="{width: `${100*json.length}%`}" 
          />
        </div>
        <div class="tw-relative">
          <MainNumber
            color="red"
            text="65489"
            mt="130"
            mb="75"
            before="к = 11,6"
            class=""/>   
          <Button v-if="index+1==json.length" icon="next" class="tw-absolute tw-top-0 tw-right-0 tw-transform tw-translate-y-1/3"/>

        </div>
        
      </div>
    </ColumnTable>

  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber from "components/MainNumber";
import BorderLine from "components/BorderLine";
import TableGradientLine from "components/TableGradientLine";
import Button from "components/Button";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber,
    BorderLine,
    TableGradientLine,
    Button
  },
  data () {
    return {
      json: [
        {
          date: 2018,
          title: 4051005,
        },
        {
          date: 2019,
          title: 4051005,
        },
        {
          date: 2020,
          title: 4051005,
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
