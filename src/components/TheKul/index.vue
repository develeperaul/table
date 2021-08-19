<template>
  <div>
    <div class=" rows">
      <div class="tw-flex tw-items-baseline">
        <span class="date-vertical">
          2020
        </span>
        <MainNumber
        text="26,254"
        color="green"
        fs="300"
        lh="300"
        mt="65"
        mb="80"/>
      </div>
    </div>
    <border-line/>
    <div class="rows">
      <div class="tw-flex tw-items-baseline">
        <span class="date-vertical ">
          2020
        </span>
        <MainNumber
        text="26,254"
        fs="300"
        lh="300"
        mt="65"
        mb="80"/>
      </div>
      <div class="visits">
        <div class="visit">
          <img width="102px" height="101px" src="./icons/books.svg" 
          class="icon tw-absolute tw-bottom-0">
          <div class="visit-content">
            <span class="visit-text">Число посещений библиотек</span>
            <MainNumber text="29,080" />
          </div>
        </div>

        <div class="visit">
          <img width="102px" height="114px" src="./icons/festive.svg" 
          class="icon tw-absolute tw-bottom-0">
          <div class="visit-content">
            <span class="visit-text">Число посещений культурно-массовых мероприятий </span>
            <MainNumber text="29,080" />
          </div>
        </div>

        <div class="visit">
          <img width="102px" height="102px" src="./icons/rest.svg" 
          class="icon tw-absolute tw-bottom-0">
          <div class="visit-content">
            <span class="visit-text">Число посещений парков культуры и отдыха</span>
            <MainNumber text="29,080" />
          </div>
        </div>

        <div class="visit">
          <img width="102px" height="102px" src="./icons/theatre.svg" 
          class="icon tw-absolute tw-bottom-0">
          <div class="visit-content">
            <span class="visit-text">Число посещений театров</span>
            <MainNumber text="29,080" />
          </div>
        </div>

        <div class="visit">
          <img width="102px" height="102px" src="./icons/museum.svg" 
          class="icon tw-absolute tw-bottom-0">
          <div class="visit-content">
            <span class="visit-text">Число посещений музеев</span>
            <MainNumber text="29,080" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BorderLine from "components/BorderLine";
import MainNumber from "components/MainNumber";

export default {
  // name: 'ComponentName',
  components:{
    MainNumber, 
    BorderLine,
    
  },
  data () {
    return {}
  }
}
</script>
<style lang="scss" scoped>
  .date-vertical{
    font-size: 40px;
    
    letter-spacing: 0.5em;
    display: inline-block;
    transform:  translate(-35%,-100%) rotate(-90deg);
    
  }
  .rows{
    
    position: relative;
    display: flex;
    
    
    
  }
  .icon {
    bottom: 25%;
    transform: translateY(25%);
  }
  .visits {
    margin-left: 228px;
    transform: translateY(65px);
  }
  .visit {
    position: relative;
    &-content{
    margin-left: 200px;
    margin-top: 47px;
    }
    &-text {
      display: inline-block;
      font-size: 30px;
      line-height: 30px;
      max-width: 450px;
      margin-bottom: 5px;
    }
  }
</style>


