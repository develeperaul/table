<template>
  <div>
    <span class="title">
      Численность населения в возрасте 3–79 лет, занимающегося физической культурой и спортом, чел
    </span>
    <MainNumber text="1819883" fs="300" lh="300" color="green"/>
  </div>
</template>

<script>
import MainNumber from "components/MainNumber";
export default {
  // name: 'ComponentName',
  components: {
    MainNumber
  },
  data () {
    return {}
  }
}
</script>
<style lang="scss" scoped>
    .title {
    font-size: 50px;
    line-height: 68.09px;
    font-weight: 700;
    display: block;
    max-width: 70%;
    margin-bottom: 45px;
  }
</style>