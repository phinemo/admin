<template>
  <div class="app-container">
    <el-form ref="form" label-position="top" :model="form" label-width="120px">
      <el-form-item label="Nama Operator">
        <el-input v-model="form.name" />
      </el-form-item>
      <el-form-item label="Media Socials" style="margin-bottom:0px" />
      <el-row :gutter="20">
        <el-col :span="6">
          <el-form-item>
            <el-input v-model="form.facebook" placeholder="Facebook" />
          </el-form-item>
        </el-col>
        <el-col :span="6">
          <el-form-item>
            <el-input v-model="form.twitter" placeholder="Twitter" />
          </el-form-item>
        </el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="6">
          <el-form-item>
            <el-input v-model="form.instagram" placeholder="Instagram" />
          </el-form-item>
        </el-col>
        <el-col :span="6">
          <el-form-item>
            <el-input v-model="form.number" placeholder="Mobile Number" />
          </el-form-item>
        </el-col>
      </el-row>
      <el-form-item label="Upload your Logo">
        <el-upload class="upload-demo" drag action="https://jsonplaceholder.typicode.com/posts/" :on-preview="handlePreview"
          :on-remove="handleRemove" :file-list="fileList" multiple>
          <i class="el-icon-upload"></i>
          <div class="el-upload__text">Drop file here or <em>click to upload</em></div>
          <div class="el-upload__tip" slot="tip">jpg/png files with a size less than 500kb</div>
        </el-upload>
      </el-form-item>
      <el-form-item label="Tell about your self">
        <el-input v-model="form.desc" type="textarea" />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">Save</el-button>
        <el-button @click="onCancel">Cancel</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
  export default {
    /* eslint-disable */
    data() {
      return {
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          facebook: '',
          twitter: '',
          instagram: '',
          number: '',
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
  .line {
    text-align: center;
  }

</style>
