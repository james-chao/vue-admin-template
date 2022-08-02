<template>
  <div class="app-container">
    <el-form ref="form" :model="form" label-width="120px">
      <!-- <el-form-item label="Material"> -->
        <el-input v-model="form.name" placeholder="please input your material" />
      <!-- </el-form-item> -->
      <!-- <el-form-item label="SKU number"> -->
        <el-select v-model="form.region" placeholder="please select your SKU">
          <el-option label="Zone one" value="shanghai" />
          <el-option label="Zone two" value="beijing" />
        </el-select>
        <el-checkbox v-model="form.type" label="Query By L11" name="type" />
      <!-- </el-form-item> -->
      <!-- <el-form-item label="Instant delivery">
        <el-switch v-model="form.delivery" />
      </el-form-item> -->
      <!-- <el-form-item label="Activity type">
        <el-checkbox-group v-model="form.type">
          <el-checkbox label="Query By L11" name="type" />
        </el-checkbox-group>
      </el-form-item> -->
      <el-form-item>
        <el-button type="primary" @click="onSubmit">Create</el-button>
        <el-button @click="onCancel">Cancel</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      }
    }
  },
  methods: {
    onSubmit() {
      this.$message('submit!')
    },
    onCancel() {
      this.$message({
        message: 'cancel!',
        type: 'warning'
      })
    }
  }
}
</script>

<style scoped>
.line{
  text-align: center;
}
</style>

