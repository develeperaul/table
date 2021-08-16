<template>
  <div class="tw-flex tw-w-full tw-relative">
    <div
      class="   tw-absolute"
      style="width: 100%; height: 20px; top: 30px;  background: linear-gradient(270deg, #00CD77 0%, #6A7186 41.01%);"
    >

    </div>
    <div
      v-for="item in 3"
      :key="item"
      class="tw-flex tw-flex-col tw-w-1/3"
    >
      <span
        class="tw-text-xl"
        style="margin-bottom: 20px"
      >2018</span>
      <div class="tw-flex tw-flex-col">
        <span class="tw-text-5xl tw-font-bold">
          47010
        </span>
        <span>
          к = 11,6
        </span>
        <span>
          1,652
        </span>
        <hr>
      </div>
      <div>
        934 198
        <hr>
      </div>
      <div>
        26
        <hr>
      </div>
      <div>
        6,3/3,8
        <hr>
      </div>
      <div>
        240 (к. 5,1)
        <hr>
      </div>

    </div>

  </div>
</template>

<script>

export default {
  name: 'MainLayout',
}
</script>
