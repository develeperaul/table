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
      </span>

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="green"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <MainNumber  color="green" text="-11111" mt="130" mb="75"/>  

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="red"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <MainNumber  color="red" text="65489" mt="130" mb="75"/>   
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

