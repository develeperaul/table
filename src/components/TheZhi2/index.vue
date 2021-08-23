<template>
  <div class="tw-flex"
  style="margin-left: 200px">
    
      <ColumnTable v-for="(item, index) in json" :key="index" v-bind="{item, index, length: json.length}" pl="83">
        <div>
          <p ref="text" class="text">
            {{item.text}}
          </p>
        </div>
        <div class="tw-relative">
          <span v-if="index==0" class="date-vertical">
            2020
          </span>
          <MainNumber :text="item.numb1" fs="200" lh="200"  trend="up" color="green"/>

        </div>
          <BorderLine
          style="margin-top:145px; margin-bottom: 110px"
          :style="{marginLeft:[index==0? '-200px' : index>0 ? '-83px': '']}"/>
        <div class="tw-relative">
          <span v-if="index==0" class="date-vertical">
            2020
          </span>
          <MainNumber :text="item.numb2" fs="200" lh="200"  color="red"/>
        </div>
        

      </ColumnTable>
    
  </div>
</template>

<script>
import ColumnTable from "components/ColumnTable";
import MainNumber  from "components/MainNumber";
import BorderLine from "components/BorderLine";
export default {
  // name: 'ComponentName',
  components: {
    ColumnTable,
    MainNumber,
    BorderLine
  },
  data () {
    return {
      json : [
        { 
          numb1: "84",
          numb2: "78,74",
          text: "Количество семей, купивших жилое помещение по договорам купли-продажи или зарегистрировавших право собственности на основании договора участия в долевом строительстве"
        },
        {
          numb1: "13,04",
          numb2: "12,5",
          text: "Количество семей, построивших индивидуальный жилой дом за счет собственных и привлеченных средств"
          
          
          
        },
        {
          
          numb1: "0,09",
          numb2: "0,365",
          text: "Количество семей, переселенных из аварийного жилищного фонда в рамках региональных адресных программ, без учета семей, которые выбрали в качестве способа переселения из аварийного жилищного фонда получение возмещения в денежной форме и семей, переселенных в жилые помещения жилищного фонда социального использования"
        }
      ]
    }
  },
  mounted(){
    const textArray = this.$refs.text;
    let Maxheight = textArray.reduce((acc, val) => {
      if(acc < val.offsetHeight) acc = val.offsetHeight 
        return acc
    }, textArray[0].offsetHeight);
    textArray.forEach(el=>el.style.height = Maxheight+'px')
    

  }
}
</script>
<style lang="scss" scoped>
  .text{
    display: inline-block;
    max-width: 594px;
    font-size: 30px;
    line-height: 30px;
    margin-bottom: 65px;
  }
  .date-vertical{
    font-size: 40px;
    position: absolute;
    letter-spacing: 0.5em;
    display: inline-block;
    transform:  translate(-35%,-100%) rotate(-90deg);
    bottom: 0;
    left: -200px;
  }
</style>