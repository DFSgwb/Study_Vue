<template>
    <div>
        <h1 v-text="msg" ref="title"></h1>
        <button ref="btn" @click="showDOM">点我输出上方的DOM元素</button>
        <School ref="sch"></School>
    </div>
</template>

<script>
    import School from './components/School'
    export default {
        name:'App',
        data() {
            return {
                msg:'欢迎学习Vue!'
            }
        },
        components:{School},
        methods: {
            showDOM(){
                console.log(this.$refs.title); //this ==> vc(app组件)
                console.log(this.$refs.btn); //发生事件的dom元素m
                console.log(this.$refs.sch); //可以是school组件加refs属性 获得的是组件事例对象vc
            }
        },
    }
</script>
