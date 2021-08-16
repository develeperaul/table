<template>
    <div class="tw-flex tw-w-full tw-relative">
    <div
      class=" tw-flex tw-items-center  tw-absolute"
      style="width: 100%;  top: 95px;  "
      :style="{ background:[colorType=='#FF0000'?  'linear-gradient(270deg, #00CD77 0%, #6A7186 41.01%);' : 'linear-gradient(270deg, #F30101 0%, #6A7186 41.01%)']}"
    >
      <span
        class=" text-gradient"
      >
        Число родившихся (в т.ч. на 1000 человек населения) 
      </span>
    </div>
    <div
      v-for="(item, index) in json"
      :key="index"
      class="tw-flex tw-flex-col "
      :class="`tw-w-1/${json.length}`"
      :style="[{background:(index+1)%2==0 ? ' rgba(196, 196, 196, 0.05)' : ''}, {paddingLeft:index>0 ? '30px': ''}]"
    >
      <span
        class="tw-text-xl date"
        style="margin-bottom: 20px"
      >2018</span>
      <div class="tw-flex tw-flex-col">
        <span class="tw-text-5xl tw-font-bold title"
        :style="{color: colorTitle}">
          47010
        </span>
        <span class="tw-mb-2 subtitle">
          к = 11,6
        </span>
          <Cell v-bind="{item: item.info, index}"/>
          
      </div>
      {{'261(10231)'.search(/[(]/)}}
    </div>
    
  </div>

</template>

<script>
import Cell from "components/Cell";
export default {
  components : {
    Cell
  },
  // name: 'ComponentName',
  props: {
    colorTitle: {
      default: '#01F859',
      type: String
    }
  },
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
  .title {
    font-size: 110px;
    line-height: 110px;
    font-weight: 700;
    margin-top: 40px;
  }
  .subtitle {
    font-size: 40px;
    line-height: 40px;
    font-weight: 600;
  }
  .text-gradient {
    font-size: 40px;
    line-height: 54.47px;
    font-weight: 400;
    margin-left: 20px;
    white-space: nowrap;
  }
</style>