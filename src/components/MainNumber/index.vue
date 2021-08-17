
<template>
<!-- Большие цифры -->
    <div class="tw-flex tw-flex-col"
    :style="[{marginTop: mt+'px'},{marginBottom: mb+'px'}]">
      <span class="subtitle">
        <slot name="after" class="subtitle"></slot>
      </span>
      <span class="tw-text-5xl tw-font-bold title"
        :style="{color: [color == 'green' ? '#01F859': color == 'red' ? '#FF0000' : '']}">
          {{text}}
      </span>
      <span class="subtitle"
      style="margin-top: 25px">
        <slot name="before"></slot>
      </span>
      <span>
        <slot name="execution"></slot>
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
    .subtitle {
      font-size: 40px;
      line-height: 40px;
      font-weight: 600;
    }
</style>