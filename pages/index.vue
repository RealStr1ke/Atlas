<template>
	<div class="container">
		<ProfileHeader />
		<div class="link-card-list">
			<ul id="item">
				<li>
					<LinkCard
						title="GitHub"
						description="All my public code is stored here"
						url="https://github.com/RealStr1ke"
						card-type="github"
						icon-name="fa-brands:github"
					/>
				</li>
				<!-- Add other link cards similarly -->
			</ul>
		</div>
	</div>
</template>

<style>
.link-card-list {
  width: 100%;
}

/* Card type styles */
.link-card-list .instagram:hover { background: #007c06; }
.link-card-list .youtube:hover { background: #FF0000; }
.link-card-list .telegram:hover { background: #0088cc; }
.link-card-list .github:hover { background: #333; }
.link-card-list .insta:hover {
  background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
}
.link-card-list .discord:hover { background: #7289DA; }
</style>