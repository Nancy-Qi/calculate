<template>
    <div>
        <el-row>
            <el-input v-model.number="number1" placeholder="请输入第一个数字" clearable></el-input>
            <el-input v-model.number="number2" placeholder="请输入第二个数字" clearable></el-input>
            <label>=</label>
            <el-input v-model="number3"></el-input>
        </el-row>
        <el-row>
            <label>请选择计算方式</label>
            <el-button type="primary" @click="add">+</el-button>
            <el-button type="success" @click="subtract">-</el-button>
            <el-button type="warning" @click="multiply">*</el-button>
            <el-button type="danger" @click="divide">/</el-button>
        </el-row>
    </div>
</template>

<script>
export default {
    name: 'calculate',
    data() {
        return {
            number1: 0,
            number2: 0,
            number3: 0
        }
    },
    methods: {
        add() {
            this.number3 = this.number1 + this.number2
        },
        subtract() {
            this.number3 = this.number1 - this.number2
        },
        multiply() {
            this.number3 = this.number1 * this.number2
        },
        divide() {
            this.number3 = this.number1 / this.number2
        }

    }

}
</script>

<style lang="scss">
.el-input {
    width: 150px;
    margin: 10px;
}

.el-button {
    margin: 10px;
}
</style>
