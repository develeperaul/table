<template>
  <div>
  <NAS1 />
  <NAS4 />
  <NAS5 />
  <PRODZHIZN1 style="margin-right:100px"/>
  <PRODZHIZN2  style="margin-right:220px"/>
  <PRODZHIZN3/>
  <PRODZHIZN4/>
  <PRODZHIZN5/>
  <ZP1/>
  
  </div>
</template>

<script>
import Table from "components/Table";
import NAS1 from "components/NAS1";
import NAS4 from "components/NAS4";
import NAS5 from "components/NAS5";
import PRODZHIZN1 from "components/PRODZHIZN1";
import PRODZHIZN2 from "components/PRODZHIZN2";
import PRODZHIZN3 from "components/PRODZHIZN3";
import PRODZHIZN4 from "components/PRODZHIZN4";
import PRODZHIZN5 from "components/PRODZHIZN5";
import ZP1 from "components/ZP1";
export default {
  name: 'MainLayout',
  components: {
    Table,
    NAS1,
    NAS4,
    NAS5,
    PRODZHIZN1,
    PRODZHIZN2,
    PRODZHIZN3,
    PRODZHIZN4,
    PRODZHIZN5,
    ZP1
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
