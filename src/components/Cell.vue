<template>
<!-- данные в ячейке -->

  <div>
    <div class="tw-flex tw-flex-col container tw-relative"
      v-for="(itemCell, indexCell) in item" :key="indexCell"> 
            <span
            v-if="index<1"
            class="tw-absolute title"
            style="white-space: nowrap;">
              {{itemCell.title}}
            </span>
            
            <span class=" subtitle"
            >
              {{itemCell.subtitle}}
              
            </span>
            <template v-if="endLine">
              <div
              style="border-bottom: 4px solid #6A7186"
              :style="{marginLeft:[index>0 ? '-30px': '']}">
              </div>
            </template>
            <template v-else>
              <div
              v-if="(indexCell+1)<item.length"  
              style="border-bottom: 4px solid #6A7186"
              :style="{marginLeft:[index>0 ? '-30px': '']}">
              </div>
            </template>

    </div>

  </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  props: {
    item: {
      type: Array,
      required: true
    },
    index: {
      type: Number,
      required: true
    },
    endLine: {
      type: Boolean,
      default: false,
    }
  },
  data () {
    return {}
  },
}
</script>
<style lang="scss" scoped>
  .container {
    margin-bottom: 20px;
  }
  .title {
    
    font-size: 27px;
    line-height: 27px;
    font-weight: 400;
  }
  .subtitle {
    margin: 40px 0 20px 0;
    font-size: 60px;
    line-height: 60px;
    font-weight: 700;
  }
</style>
