<template>
	<div class="container-fluid">
		<div class="col-12">
			<div class="row">
				<div style="padding: 0px;" class="col-sm-12 col-md-4">
					<!--left-->
					<div class="left">
						<div class="leftright_bg">
							<Left />
						</div>
					</div>
				</div>

				<div style="padding: 10px;" class="col-sm-12 col-md-4 mobile_col2 center_col">
					<!--main-->
					<div class="nav nav-pills">
						<a style="padding: 0px;" v-for="(item, index) in menuItems" :key="index"
							:class="['nav-link', { active: activeIndex === index }]"
							@click="setActive(index, item.componentId)">
							<img :src="activeIndex === index ? item.activeSrc : item.inactiveSrc" :alt="item.name"
								class="img-fluid" />
						</a>
					</div>
					<hr style="color: white;">

					<!-- 将 id 放在外层 div 上 -->
					<div :id="menuItems[0].componentId">
						<component :is="currentComponent"></component>
					</div>

					<div style="padding-bottom: 100px;" class="content" :id="menuItems[1].componentId">
						<Content />
					</div>

				</div>

				<div style="padding: 0px;" class="col-sm-12 col-md-4 mobile_col">
					<!--right-->
					<div class="right">
						<div class="right_bg">
							<Right />
						</div>
					</div>
				</div>

			</div>
		</div>
	</div>
</template>

<script>
import Left from '../components/Left.vue';
import Right from '../components/Rightt.vue';
import Menu1 from '../components/contenttt.vue';
import Content from '@/components/Menuu.vue';

export default {
	name: 'Home',
	components: {
		Left,
		Right,
		Menu1,
		Content
	},
	data() {
		return {
			activeIndex: 0,
			menuItems: [
				{ name: 'Menu 1', activeSrc: '/image_main/spribe.gif', inactiveSrc: '/image_main/spribe.gif', component: 'Menu1', componentId: 'menu1' },
				{ name: 'Menu 2', activeSrc: '/image_main/slotgame.gif', inactiveSrc: '/image_main/slotgame.gif', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 3', activeSrc: '/image_main/minigame.webp', inactiveSrc: '/image_main/minigame.webp', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 4', activeSrc: '/image_main/livecasino.webp', inactiveSrc: '/image_main/livecasino.webp', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 5', activeSrc: '/image_main/sportbook.webp', inactiveSrc: '/image_main/sportbook.webp', component: 'Menu1', componentId: 'content' },
			],
		};
	},
	computed: {
		currentComponent() {
			return this.menuItems[this.activeIndex].component;
		}
	},
	methods: {
		setActive(index, componentId) {
			this.activeIndex = index;
			if (index === 0) {
				this.scrollTo(componentId);
			} else {
				this.scrollTo('content');
			}
		},
		scrollTo(id) {
			const element = document.getElementById(id);
			if (element) {
				element.scrollIntoView({ behavior: 'smooth' });
			}
		},
	},
};
</script>

<style scoped>
.center_col {
	background-color: black;
}


.leftright_bg {
	background: rgba(0, 0, 0, .3);
	height: 100%;
	border-right: 1px solid rgba(255, 255, 255, .5);
}

.left {
	height: 100%;
	background-color: black;

}

.right_bg {
	background: rgba(0, 0, 0, .3);
	height: 100%;
	border-left: 1px solid rgba(255, 255, 255, .5);
}

.right {
	height: 100%;
	background-color: black;
}


@media (max-width: 768px) {

	.leftright_bg {
		background: rgba(0, 0, 0, 0);
		height: 100%;
		border-right: 0px solid rgba(255, 255, 255, .5);
	}

	.right_bg {
		background: rgba(0, 0, 0, 0);
		height: 100%;
		border-left: 0px solid rgba(255, 255, 255, .5);
	}

	.nav-pills {
		display: flex;
		overflow-x: auto;
		/* 启用水平滚动 */
		white-space: nowrap;
		/* 防止换行 */
		padding: 0;
	}

	.nav-link {
		flex: 0 0 auto;
		/* 确保菜单项不变形 */
		width: 20%;
		/* 每个菜单项的宽度，假设有5个菜单项 */
		text-align: center;
		padding: 0;
	}

	.left {
		padding-bottom: 0px;
	}
}

.icon_col {
	display: flex;
	flex-direction: column;
	width: 20px;
	position: fixed;
	bottom: 100px;
	right: 0px;
}



.icon {
	display: grid;
	position: absolute;
	gap: 0.5rem;
}

.nav-item {
	font-weight: bolder;
}

.nav-pills {
	--bs-nav-pills-link-active-bg: none;
	display: flex;
	flex-wrap: nowrap;
	padding: 10px 10px 10px 10px;

}


.nav-link.active {
	border-radius: 30px;
}

.menu_col {
	padding-bottom: 10px;
}

.main-col {
	display: grid;
	grid-template-columns: repeat(5, 1fr);
	justify-items: center;
	gap: 0.5rem;
}

.main-col img {
	width: 90%;
}

@media screen and (max-width:768px) {
	.main-col {
		grid-template-columns: repeat(3, 1fr);
	}


}

@media screen and (max-width:767px) {
	.mobile_col {
		order: 2;
	}

	.mobile_col2 {
		order: 3;
	}


}

.content {
	padding-left: 12px;
	padding-right: 12px;
}

h1 {
	font-size: 25px;
	font-weight: bolder;
}

h2 {
	font-size: 23px;
	font-weight: bolder;
}

h3 {
	font-size: 15px;
	font-weight: bolder;
}

.icon_col {
	display: flex;
	flex-direction: column;
	width: 20px;
	position: fixed;
	bottom: 120px;
	right: 0px;
}

.nav-pills {
	display: flex;
	flex-wrap: nowrap;
	padding: 0;
	overflow-x: auto;
	/* 启用水平滚动 */
	white-space: nowrap;
	/* 防止换行 */
}

.nav-link {
	flex: 1;
	/* 使菜单项均匀分布 */
	text-align: center;
	padding: 0;
}

@media (max-width: 768px) {
	.nav-pills {
		flex-direction: row;
		/* 确保菜单项在水平行中 */
	}

	.nav-link {
		flex: 1;
		/* 每个菜单项占用相等的空间 */
		width: 20%;
		/* 可根据需要调整宽度 */
	}

	.center_col {
		padding-top: 20px !important;
	}
}

@media (max-width: 767px) {
	.mobile_col {
		order: 2;
	}

	.mobile_col2 {
		order: 3;
	}
}
</style>
