<template lang="html">
  <div class="page">
    <el-row :gutter="20">
      <el-col :span="5">企业名称
        <el-input v-model="input1" placeholder="请输入内容" style="width:60%;"></el-input>
      </el-col>
      <el-col :span="5">三证状态
        <el-select v-model="select1" placeholder="请选择">
          <el-option
            v-for="item in options"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
      </el-col>
      <el-col :span="5">授权书状态
        <el-select v-model="select2" placeholder="请选择">
          <el-option
            v-for="item in options2"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
      </el-col>
      <el-col :span="5">联系人
        <el-input v-model="input2" placeholder="请输入内容" style="width:60%;"></el-input>
      </el-col>
      <el-col :span="4">
        <el-button type="primary">搜索</el-button>
      </el-col>
    </el-row>
    <el-tabs v-model="tabActive">
      <el-tab-pane label="待审核" name="first">
        <el-table :data="tableData" style="width:100%">
          <el-table-column prop="companyName" label="企业名称" width="210"></el-table-column>
          <el-table-column prop="linkMan" label="联系人" width="210"></el-table-column>
          <el-table-column prop="phone" label="联系方式" width="210"></el-table-column>
          <el-table-column prop="szstatus" label="三证状态" width="210"></el-table-column>
          <el-table-column prop="sqsstatus" label="授权书状态" width="210"></el-table-column>
          <el-table-column prop="time" label="创建时间" width="210"></el-table-column>
          <el-table-column label="操作" width="180">
            <template scope="scope">
              <el-button type="text" size="small">查看</el-button>
            </template>
          </el-table-column>
        </el-table>
      </el-tab-pane>
      <el-tab-pane label="企业" name="second">企业</el-tab-pane>
      <el-tab-pane label="人员" name="third">人员</el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input1: '',
      input2: '',
      select1: '',
      select2: '',
      tabActive: 'first',
      options: [{
        value: 1,
        label: '已认证',
      }, {
        value: 2,
        label: '未认证',
      }],
      options2: [{
        value: 1,
        label: '已授权',
      }, {
        value: 2,
        label: '未授权',
      }],
      tableData: [{
        companyName: '公司1',
        linkMan: '联系人1',
        phone: 12345678901,
        szstatus: '待审核',
        sqsstatus: '未上传',
        time: '2017-02-30',
      }, {
        companyName: '公司2',
        linkMan: '联系人2',
        phone: 12345678901,
        szstatus: '待审核',
        sqsstatus: '未上传',
        time: '2017-02-30',
      }, {
        companyName: '公司3',
        linkMan: '联系人3',
        phone: 12345678901,
        szstatus: '待审核',
        sqsstatus: '未上传',
        time: '2017-02-30',
      }, {
        companyName: '公司4',
        linkMan: '联系人4',
        phone: 12345678901,
        szstatus: '待审核',
        sqsstatus: '未上传',
        time: '2017-02-30',
      }, {
        companyName: '公司5',
        linkMan: '联系人5',
        phone: 12345678901,
        szstatus: '待审核',
        sqsstatus: '未上传',
        time: '2017-02-30',
      }],
    };
  },
};
</script>

<style lang="scss" scoped>
.page {
  width:100%;
  padding: 20px;
}
</style>