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
      <div class="tw-relative">
        <MainNumber  color="green" text="-11111" mt="130" mb="75"/>  
        <div v-if="index+1==json.length" class="people">
          <div class="tw-relative"
          style="margin-bottom: 28px">
            <img
              width="34px"
              height="72px"
              src="../MainNumber/icons/man.svg">
            <span class="people-text ">16-59</span>
          </div>
          <div class="tw-relative">
            <img
              width="34px"
              height="72px"
              
              src="../MainNumber/icons/woman.svg">
            <span class=" people-text ">16-59</span>
          </div>
        </div>
      </div>

      <div class="tw-w-full tw-relative">
        <TableGradientLine v-if="index<1" colorGradient="red"
        text="Миграционный прирост"
        class="tw-absolute"
      :style="{width: `${100*json.length}%`}" 
        />
      </div>
      <div class="tw-relative">
        <MainNumber  color="red" text="65489" mt="130" mb="75"/>   
        <div v-if="index+1==json.length" class="people">
          <div class="tw-relative"
          style="margin-bottom: 28px">
            <img
              width="34px"
              height="72px"
              src="../MainNumber/icons/man.svg">
            <span class="people-text">60+</span>
          </div>
          <div class="tw-relative">
            <img
              width="34px"
              height="72px"
              
              src="../MainNumber/icons/woman.svg">
            <span class="people-text">55+</span>
          </div>
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
   &-text {
     font-size: 30px;
     line-height: 30px;
     font-weight: 700;
     white-space: nowrap;
     position: absolute;
     top: 50%;
     transform: translateY(-50%);
     left: 100%;
     margin-left: 15px;
     
   } 
 }
</style>

