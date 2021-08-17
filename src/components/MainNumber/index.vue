
<template>
<!-- Большие цифры -->
    <div class="tw-flex tw-flex-col"
    :style="[{marginTop: mt+'px'},{marginBottom: mb+'px'}]">
      <span 
      v-if="after"
      class="subtitle">
        <!-- <slot name="after" class="subtitle"></slot> -->
        {{after}}
      </span>
      <span class="tw-text-5xl tw-font-bold title"
        :style="{color: [color == 'green' ? '#01F859': color == 'red' ? '#FF0000' : '']}">
          {{text}}
      
        <img 
        v-if="execution"
        class="tw-inline-block tw-align-baseline"
        style="margin-left: 60px"
        :src="require('./icons/' + execution + '.svg')">
      </span>
      <span class="subtitle"
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
      required: true,
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
    after: {
      required: false,
      type: String
    },
    before: {
      required: false,
      type: String
    },

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
    .subtitle {
      font-size: 40px;
      line-height: 40px;
      font-weight: 600;
      margin-bottom: 20px;
      margin-left: 6px;
    }
</style>