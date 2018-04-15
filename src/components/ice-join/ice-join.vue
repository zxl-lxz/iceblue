<template>
  <div class="join" id="join">
    <el-form ref="form" :model="form" label-width="100px">
      <el-form-item label="姓名">
        <el-input v-model="form.name"></el-input>
      </el-form-item>
      <el-form-item label="性别">
        <el-select v-model="form.region" placeholder="请选择性别">
          <el-option label="帅哥" value="man"></el-option>
          <el-option label="美女" value="women"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="在校时间">
        <el-col :span="11">
          <el-date-picker type="date" placeholder="入学时间" v-model="form.date1" style="width: 100%;"></el-date-picker>
        </el-col>
        <el-col class="line" :span="2">-</el-col>
        <el-col :span="11">
          <el-date-picker type="date" placeholder="毕业时间" v-model="form.date2" style="width: 100%;"></el-date-picker>
        </el-col>
      </el-form-item>
      <el-form-item label="我有特长">
        <el-switch v-model="form.delivery"></el-switch>
      </el-form-item>
      <el-form-item label="兴趣方向">
        <el-checkbox-group v-model="form.type">
          <el-checkbox label="前端开发FED" name="type"></el-checkbox>
          <el-checkbox label="后端开发" name="type"></el-checkbox>
          <el-checkbox label="UI设计师" name="type"></el-checkbox>
          <el-checkbox label="PM产品经理" name="type"></el-checkbox>
        </el-checkbox-group>
      </el-form-item>
      <el-form-item label="基础有伐？">
        <el-radio-group v-model="form.resource">
          <el-radio label="有一些"></el-radio>
          <el-radio label="我是零基础"></el-radio>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="随便聊聊">
        <el-input type="textarea" v-model="form.desc"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">可以申请加入啦</el-button>
        <el-button>再想想</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  data () {
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
    onSubmit () {
      alert('test')
    }
  }
}
</script>

<style scoped>
.join {
  height: 100%;
}
form {
  width: 800px;
  margin: 0 auto;
  padding-top: 160px;
}
</style>
