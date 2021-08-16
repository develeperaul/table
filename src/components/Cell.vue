<template>
  <div>
    <div class="tw-flex tw-flex-col tw-relative container"
    v-for="(i, indexCell) in item" :key="indexCell">
          <span
          v-if="index<1"
          class="tw-absolute title"
          style="white-space: nowrap;">
            {{i.title}}
          </span>
          
          <span class=" subtitle"
          >
            {{i.subtitle}}
            
          </span>
          <div
          v-if="(indexCell+1)<item.length"  
          style="border-bottom: 4px solid #6A7186"
          :style="{marginLeft:[index>0 ? '-30px': '']}">
            
          </div>
        
    </div>
  </div>
</template>

<script>

export default {
  props: {
    item: {
      required: true,
      type: Object
    },
    index: {
      required: true,
      type: Number
    },

  },
  // name: 'ComponentName',
  data () {
    return {
      json: [
        {
          title: 'суммарный коэффициент рождаемости',
          subtitle: '1,652'
        }
      ]
    }
  }
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
