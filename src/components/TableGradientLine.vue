<template>
<!-- градиентная линия -->
  <div
      class=" tw-flex tw-items-center  "
      style="width: 100%; min-height: 80px;"  
      :style="{ background:[colorGradient=='green'? 'linear-gradient(270deg, #00CD77 0%, #6A7186 41.01%)' : colorGradient=='red' ? 'linear-gradient(270deg, #F30101 0%, #6A7186 41.01%)' : '']}"
    >
      <span
        class=" text-gradient"
      >
        {{text}}
      </span>
    </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  props: {
    colorGradient: {
      required: true,
      type: String
    },
    text: {
      required: true,
      type: String
    },
    
  },
  data () {
    return {}
  }
}
</script>
<style lang="scss" scoped>
    .text-gradient {
    font-size: 40px;
    line-height: 54.47px;
    font-weight: 400;
    margin-left: 20px;
    max-width: 72%;
    padding-bottom: 5px;
    // white-space: nowrap;
  }
</style>
