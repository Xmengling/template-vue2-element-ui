<template>
  <div class="hello">
    <div class="button">
      <el-button>组件按钮</el-button>
    </div>
    <el-button @click="apiTestApi">api请求</el-button>
  </div>
</template>

<script>
import { apiTest } from '@/api/hello-world'
export default {
  name: 'HelloWorld',
  components: {

  },
  methods: {
    async apiTestApi() {
      try {
        await apiTest()
      } catch (error) {
        throw new Error()
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.hello {
  .button {
    font-size: 18px;
  }
}
</style>
