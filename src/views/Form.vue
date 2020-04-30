<template>
  <el-row>
    <el-col :span="18" :offset="3">
      <div class="card-wrapper">
        <el-card class="box-card" v-for="(card, i) in cards" :key="i">
          <div slot="header" class="card-header">
            <span>Add Task</span>
            <el-button type="text">Submit</el-button>
          </div>

          <div class="text item">
            <el-input placeholder="Name" v-model="inputs[i]" />
            <el-input
              type="textarea"
              placeholder="Description"
              v-model="textareas[i]"
              maxlength="30"
              show-word-limit
            />
          </div>
          <!-- <el-button type="primary" @click="onSubmit">Create</el-button>
          <el-button>Cancel</el-button> -->
        </el-card>
      </div>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data() {
    return {
      cards: [...Array(1).keys()],
      inputs: [],
      textareas: []
    }
  }
}
</script>

<style scoped>
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.card-header button {
  padding: 2px 5px;
  margin: 0;
}
.card-wrapper {
  display: flex;
  flex-wrap: wrap;
  margin: 10px;
}
.el-card {
  width: 300px;
  margin: 5px;
}
.el-textarea {
  margin-top: 10px;
}
.el-button {
  margin-top: 10px;
}
</style>
