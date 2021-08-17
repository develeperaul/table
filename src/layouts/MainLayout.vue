<template>
  <!-- <Table colorTitle="#FF0000" colorGradient="green"/> -->
  <div>

  <NAS1 />
  <!-- <PRODZHIZN1/> -->
  </div>
</template>

<script>
import Table from "components/Table";
import NAS1 from "components/NAS1";
import PRODZHIZN1 from "components/PRODZHIZN1"
export default {
  name: 'MainLayout',
  components: {
    Table,
    NAS1,
    PRODZHIZN1
  }
}
</script>
<style lang="scss" >
    .date {
    font-size: 50px;
    font-weight: 700;
    line-height: 68.09px;
    margin-bottom: 75px;
    
    margin-top: 21px;
  }
</style>
