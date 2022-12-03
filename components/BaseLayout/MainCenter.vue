<template>
  <div class="main-center">
    <div class="left-logo">12</div>
    <div class="center-search">
      <div class="top-input">
        <el-input placeholder="请输入内容" v-model="input2">
          <template slot="append">
            <el-button icon="el-icon-search" type="warning">搜索</el-button>
          </template>
        </el-input>
      </div>
      <div class="botm-wrap">
        <div class="btom-hot-wrords">
          <template v-for="(item, index) in tags">
            <div class="tag-items">
              <el-tag :type="item.type">{{ item.name }}</el-tag>
            </div>
          </template>
        </div>

        <div class="more-wrords">
          <a href="">更多...</a>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "MainCenter",

  data() {
    return {
      input2: '长袖女',
      tags: [
        {name: '手提包', type: 'danger'},
        {name: '帆布鞋', type: 'success'},
        {name: '男腰包', type: 'warning'},
        {name: '休闲鞋', type: 'info'},
        {name: '零食', type: 'info'},
        {name: '裤子男', type: 'info'},
        {name: '打底裤', type: 'info'},
        {name: '衬衣男', type: 'info'},
        {name: '真皮女包单肩包', type: 'info'}
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.main-center {
  padding-top: 20px;
  @extend .flex-center;

  .left-logo {
    width: 15%;
    height: 120px;
    margin-right: 100px;
    background-color: $base-color;
  }

  .center-search {
    width: 60%;
  }

  .botm-wrap {
    justify-content: space-around;
    @extend .flex-center;
  }

  .btom-hot-wrords, .more-wrords {
    margin-top: 10px;
  }

  .btom-hot-wrords {
    @extend .flex-center;

    .tag-items {
      cursor: pointer;
      margin-right: 5px;
    }
  }

}
</style>
