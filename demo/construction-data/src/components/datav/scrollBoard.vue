<template>
  <div id="scroll-board" style="height:98%;background-color: #091a2d;">
       <!-- <div class="table-name">
        <img src="./img/icon1.png" />人员贡献排行榜
      </div> -->

    <dv-scroll-board :config="config"  @click="testClick"/>
  </div>
</template>

<script>
export default {
  name: 'ScrollBoard',
  data () {
    return {
      config: {
        header: ['站点', '报警描述'],
        data: [
          ['站点0001', '这是一条报警描述1'],
          ['站点0002', '这是一条报警描述1'],
          ['站点0003', '这是一条报警描述1'],
          ['站点0004', '这是一条报警描述1'],
          ['站点0005', '这是一条报警描述1'],
          ['站点0006', '这是一条报警描述1'],
          ['站点0007', '这是一条报警描述1'],
          ['站点0008', '这是一条报警描述1'],
          ['站点0009', '这是一条报警描述1'],
          ['站点0010', '这是一条报警描述1'],
          ['站点0011', '这是一条报警描述1'],
          ['站点0012', '这是一条报警描述1'],
          ['站点0013', '这是一条报警描述1'],
          ['站点0014', '这是一条报警描述1'],
          ['站点0015', '这是一条报警描述1'],
          ['站点0016', '这是一条报警描述1'],
          ['站点0017', '这是一条报警描述1'],
          ['站点0018', '这是一条报警描述1'],
          ['站点0019', '这是一条报警描述1'],
          ['站点0020', '这是一条报警描述1'],
          ['站点0021', '这是一条报警描述1'],
          ['站点0022', '这是一条报警描述1'],
          ['站点0023', '这是一条报警描述1'],
          ['站点0024', '这是一条报警描述1'],
          ['站点0025', '这是一条报警描述1'],
          // ['2019-07-02 17:25:00', '路面危害-路面油污清理', '13', 'xxxxxxx'],

        ],
        index: true,
        columnWidth: [65, 110],
        align: ['center'],
        rowNum: 20,
        headerBGC: '#1981f6',
        headerHeight: 45,
        oddRowBGC: 'rgba(0, 44, 81, 0.8)',
        evenRowBGC: 'rgba(10, 29, 50, 0.8)',
        carousel:'single',
        indexHeader:'序号'
      }
    }
  },
 methods: {
   //预留后面用来展示报警的具体信息
    testClick(row,ceil,rowIndex,columnIndex) {
      console.log(row)
      console.log(row.ceil)
      console.log(row.rowIndex)
      console.log(row.columnIndex)
    },
  }
}
</script>

<style lang="less">
#scroll-board {
  width: 98%;
  box-sizing: border-box;
  margin-left: 20px;
  height: 100%;
  overflow: hidden;

}
  .table-name {
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 5px;

    img {
      width: 25px;
      height: 25px;
      margin-right: 5px;
    }
  }

</style>
