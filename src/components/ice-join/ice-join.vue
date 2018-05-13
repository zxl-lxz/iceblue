/*
 * @Author: liang.zhou
 * @Date: 2018-04-19 22:30:35
 * @Last Modified by: liang.zhou
 * @Last Modified time: 2018-05-12 16:00:36
 */

<template src="./index.html">
</template>

<script type="text/ecmascript-6">
export default {
	data() {
		return {
			formShow: false,
			form: {
				name: '',
				school: '',
				major:'',
				start_time: '',
				end_time: '',
				sex: '',
				interest: [],
				tel: '',
				message: ''
			},
			iconLists: [
				{
					name: '前端开发',
					iconName: 'icon-qianduan',
				},
				{
					name: '后台开发',
					iconName: 'icon-houduankaifa'
				},
				{
					name: 'Andriod',
					iconName: 'icon-anzhuo',
				},
				{
					name: 'IOS',
					iconName: 'icon-iOS'
				},
				{
					name: '新媒体运营',
					iconName: 'icon-icon12'
				},
				{
					name: '产品经理',
					iconName: 'icon-chanpinjingli'
				},
				{
					name: 'UI设计',
					iconName: 'icon-UIsheji'
				},
				{
					name: '测试',
					iconName: 'icon-app'
				}
			],
			rules: {
				name: [
					{required: true, message: '请输入名字', trigger: 'blur'},
					{min: 2, max: 5, message: '长度在2到5之间哦', trigger: 'blur'}
				],
				school: [
					{required: true, message: '请输入学校名称', trigger: 'blur'}
				],
				major: [
					{required: true, message: '请输入专业名称', trigger: 'blur'}
				],
				start_time: [
					{type: 'date', required: true, message: '请选择入学日期', trigger: 'change'}
				],
				end_time: [
					{type: 'date', required: true, message: '请选择毕业日期', trigger: 'change'}
				],
				sex: [
					{required: true, message: '请选择性别', trigger: 'change'}
				],
				interest: [
					{type: 'array', required: true, message: '请至少选择一个兴趣方向', trigger: 'change'}
				],
				tel: [
					{required: true, message: '请输入11位电话号码', len: 11, trigger: 'blur'}
				],
				message: [
					{required: true, message: '简单介绍下自己~', trigger: 'blur'}
				]
			}
		};
	},
	methods: {
		onSubmit() {
			// for ( let key in this.form) {
			// 	if (!this.form[key]) {
			// 		return
			// 	}
			// }
			this.form.start_time = new Date(this.form.start_time).getTime()/1000
			this.form.end_time = new Date(this.form.end_time).getTime()/1000
			console.log(this.form.start_time)
			console.log(isNaN(this.form.start_time))
		  $.ajax({
			url: 'http://125.220.215.187/ibadmin/public/index.php/json',
			type: 'post',
			data: this.form,
			dataType: 'json',
			success: data => {
				if (data.success) {
					this.$message({
						showClose: true,
						message: data.message,
						type: 'success'
					})
					this.formShow = false;
				} else {
					this.$message({
						showClose: true,
						message: data.message,
						type: 'error'
					})
				}
			},
			error: data => {
				this.$message({
					showClose: true,
					message: data.responseText,
					type: 'error'
				})
			}
      	})
		},
		close () {
			this.formShow = false
		}
	}
};
</script>

<style lang="less" rel="stylesheet/less" src="./index.less" scoped>
</style>
