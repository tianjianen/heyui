<template>
  <DropdownMenu @click="trigger" :datas="param" @show="show" @hide="hide" placement="bottom-end" class-name="h-text-dropdown">
    <span>Menu menu</span>
  </DropdownMenu>
</template>
<script>
export default {
  data() {
    return {
      param: [
        { title: 'Test 1', key: 'test1' },
        { title: 'Test 2', key: 'test2' },
        { title: 'Test 3', key: 'test3' }
      ]
    };
  },
  methods: {
    trigger(code) {
      this.$Message.info(`You clicked ${code}`);
    },
    show() {
      this.$Message.info('Expand');
    },
    hide() {
      this.$Message.info('shut down');
    }
  }
};
</script>
