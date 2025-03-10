<template>
	<li :class="['link-card', cardType]">
		<a
			:href="url"
			target="_blank"
		>
			<span>
				<h3 :style="titleStyle">{{ title }}</h3>
				<p :style="descriptionStyle">{{ description }}</p>
			</span>
			<Icon
				:name="iconName"
				:style="iconStyle"
			/>
		</a>
	</li>
</template>

<script setup>
defineProps({
	title: String,
	description: String,
	url: String,
	cardType: {
		type: String,
		default: 'default',
	},
	iconName: String,
	titleStyle: Object,
	descriptionStyle: Object,
	iconStyle: {
		type: Object,
		default: () => ({
			color: '#ffffff',
			position: 'absolute',
		}),
	},
});
</script>

<style scoped>
.link-card {
	width: 100%;
	margin: 1.2rem 0;
	padding: 0.4rem 0.8rem;
	background: rgba(255, 255, 255, 0.1);
	backdrop-filter: blur(0px);
	border-radius: 5px;
	transition: background 0.25s;
	transform-style: preserve-3d;
	perspective: 500px;
	box-shadow: 0 0 0.8rem rgba(255, 255, 255, 0.12);
}

.link-card a {
	width: 100%;
	display: flex;
	align-items: center;
	color: #ffff;
	font-size: 1rem;
}

.link-card a i {
	text-align: center;
	line-height: 4rem;
	font-size: 1.8rem;
	text-shadow: 2px 2px 12px rgba(0, 0, 0, 0.5);
	transform: scale(1.4) translateZ(50px);
	transition: 0.25s;
	margin-left: 85%;
}

.link-card a span {
	line-height: 1.4rem;
}

@media (max-width: 1000px) {
	.link-card a span {
		line-height: 3rem;
	}
	.link-card a i {
		margin-left: 80%;
	}
}
</style>