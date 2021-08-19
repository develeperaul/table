
<template>
<!-- Большие цифры -->
    
    <div class="tw-flex tw-flex-col "
    :style="[{marginTop: mt+'px'},{marginBottom: mb+'px'}]">
    
      <span 
      v-if="after"
      class="after"
      :style="{opacity: after==true? 0 : after}">
        <!-- <slot name="after" class="subtitle"></slot> -->
        {{after}}
      </span>
        
      <span class="tw-text-5xl tw-font-bold title"
        :style="[{color: [color == 'green' ? '#01F859': color == 'red' ? '#FF0000' : color == 'orange' ? '#FF4D00' : '']},{fontSize: fs+'px'}, {lineHeight: lh+'px'}]">
          {{text}}
      
        <img 
          v-if="trend"
          class="tw-inline-block tw-align-baseline"
          :src="require('./icons/trend' + trend + '.svg')">
        
        <img 
          v-if="execution"
          class="tw-inline-block tw-align-baseline"
          style="margin-left: 60px"
          :src="require('./icons/' + execution + '.svg')">
        
        
      </span>
      <span class="before"
      v-if="before"
      style="margin-top: 25px">
        {{before}}
      </span>
      
      
    </div>  
</template>

<script>
export default {
  
  name: 'MainNumber',
  props: {
    color: {
      required: false,
      type: String
    },
    text: {
      default: '-',
      type: String
    },
    mt: {
      default: '0',
      type: String
    },
    mb: {
      default: '0',
      type: String
    },

    execution: {
      required: false,
      type: String
    },
    trend: {
      required: false,
      type: String
    },
    after: {
      required: false,
      type: String | Boolean
    },
    before: {
      required: false,
      type: String
    },
    fs: {
      default: '110',
      type: String
    },
    lh: {
      default: '110',
      type: String
    }

  }, 
  data () {
    return {}
  }
}
</script>
<style lang="scss" scoped>
    .title {
      font-size: 110px;
      line-height: 110px;
      font-weight: 700;
      
    }
    .after {
      font-size: 27px;
      line-height: 27px;
      font-weight: 400;
      margin-bottom: 10px;
      margin-left: 6px;
    }
    .before {
      font-size: 40px;
      line-height: 40px;
      font-weight: 600;
      margin-bottom: 20px;
      margin-left: 6px;
    }
</style>