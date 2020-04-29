<template>
  <el-row>
    <el-col :span="12" :offset="6">
      <el-table
        :data="tableData"
        style="width: 100%"
        class="grid-content"
      >
        <el-table-column
          fixed
          type="selection"
          width="55"
        />
        <el-table-column
          v-for="(col, i) in columns"
          :key="i"
          :prop="col"
          :label="col"
          width="150"
        >
          <template slot-scope="scope">
            <span style="margin-left: 10px">{{scope.row[col]}}</span>
            <el-dropdown>
              <span class="el-dropdown-link">
                <i class="el-icon-edit"></i>
              </span>
              <el-dropdown-menu slot="dropdown">
                <el-dropdown-item>Action 1</el-dropdown-item>
                <el-dropdown-item>Action 2</el-dropdown-item>
                <el-dropdown-item>Action 3</el-dropdown-item>
                <el-dropdown-item disabled>Action 4</el-dropdown-item>
                <el-dropdown-item divided>Action 5</el-dropdown-item>
              </el-dropdown-menu>
            </el-dropdown>
          </template>
        </el-table-column>
      </el-table>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data() {
    return {
      columns: ['date', 'name', 'state', 'city', 'address', 'zip'],
      tableData: [{
        date: '2016-05-03',
        name: 'Tom',
        state: 'California',
        city: 'Los Angeles',
        address: 'No. 189, Grove St, Los Angeles',
        zip: 'CA 90036',
        tag: 'Home'
      }, {
        date: '2016-05-02',
        name: 'Tom',
        state: 'California',
        city: 'Los Angeles',
        address: 'No. 189, Grove St, Los Angeles',
        zip: 'CA 90036',
        tag: 'Office'
      }, {
        date: '2016-05-04',
        name: 'Tom',
        state: 'California',
        city: 'Los Angeles',
        address: 'No. 189, Grove St, Los Angeles',
        zip: 'CA 90036',
        tag: 'Home'
      }, {
        date: '2016-05-01',
        name: 'Tom',
        state: 'California',
        city: 'Los Angeles',
        address: 'No. 189, Grove St, Los Angeles',
        zip: 'CA 90036',
        tag: 'Office'
      }]
    }
  },
  methods: {
    handleClick() {
      console.log('click')
    }
  }
}
</script>

<style scoped>
.el-icon-edit {
  margin-left: 4px;
}
</style>
