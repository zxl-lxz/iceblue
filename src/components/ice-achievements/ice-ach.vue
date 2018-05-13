<template src="./index.html">
</template>

<script>
export default {
  data() {
	 return {
		topCardList: [
		  {
				color: '#34acda',
				iconName: 'icon-app',
				defaultDesc: "珍题库APP",
				english: "Treasures Questions App",
				activeDesc:
					"珍题库是一款公务员行测题库app，是冰蓝和南京大学教师合作的真对公务员真题演练的项目。珍题库的设计页面为绿色，绿色会给人一种放松的感觉。其主页面分为学习，笔记本，模拟测试，收藏夹等一系列板块，用不同的颜色区分，像win8的界面，这样依据受众对色彩的敏感程度会迅速找到自己需要的板块。"
		  },
		  {
				color: '#ec0b2b',
				iconName: 'icon-hua',
				defaultDesc: "冰晶花项目",
				english: "Ice crystal flower",
				activeDesc:
					"冰晶花项目是由冰蓝工作室一期优秀学员刘琦带领团队与某大学的成员组建的团队，经过不懈的努力将艺术与科技相结合得出此美的化身：冰晶花。冰晶花（Limpidity Flower）也叫水晶花、冰莹花，又叫“永不凋谢的纯真”。"
			},
		],
		botCardList: [
			{
				color: '#bb7b1c',
				iconName: 'icon-shouceziliao',
				defaultDesc: "成长手册",
				english: "manual",
				activeDesc: "《成长手册》获全国多家媒体报道，并得到省委书记的关注.关心关爱大学生成长的电信手册获得全国多家媒体的大力宣传，并荣幸得到了国务委员刘延东同志和湖北省委书记李鸿忠同志的关注"
		  },
		  {
				color: '#596732',
				iconName: 'icon-pc',
				defaultDesc: "触点餐",
				english: "Touch point meal",
				activeDesc:
				"触点餐系统项目是由冰蓝工作室一期优秀学员龚杰带领团队，在刘俐等专业老师的指导下通过开发的一种基于二维码技术的电子点餐方法及系统。我们通过该项目实现强化学生创新创业能力的训练，增强高校学生的创新能力和在创新基础上的创业能力，培养适应创新型国家建设需要的高水平人才。"
		  }
		]
	 };
  }
};
</script>

<style lang="less" rel="stylesheet/less" src="./index.less" scoped>
</style>
