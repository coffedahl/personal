<script lang="ts">
	import type { LayoutServerData } from './$types';
	export let data: LayoutServerData;
</script>

<header class="flex items-center justify-between">
	<a href="/" class="flex items-center">
		<img src="/Logo.png" alt="" />
		<h1>Coffe Dahl</h1>
	</a>
	<nav class="navigation">
		<ul class="flex">
			<li><a href="/">Home</a></li>
			<li><a href="/web">Webdesign</a></li>
			<li><a href="/photography">Photograpy</a></li>
			<li><a href="/contact">Contact</a></li>
			{#if data.isAdmin}
				<li><a href="/admin">Admin</a></li>
			{/if}
		</ul>
	</nav>
</header>

<section>
	<slot />
</section>

<footer class="flex flex-column items-center justify-even">
	<div class="social-links flex justify-between items-center">
		<a href="https://www.instagram.com/coffedahl"><i class="fa-brands fa-instagram fa-2xl" /></a>
		<a href="https://www.linkedin.com/in/christoffer-dahl-a5b64316a/"
			><i class="fa-brands fa-linkedin fa-2xl" /></a
		>
		<a href="mailto:coffedahl@hotmail.com"><i class="fa-regular fa-envelope fa-2xl" /></a>
	</div>
	<p>©Christoffer Dahl, 2023</p>
</footer>

<style lang="scss">
	header {
		height: 10vh;
		padding: 0 5vw;
		background-color: rgba(255, 255, 255, 0);
		img {
			height: 5vh;
			margin-right: 1vw;
		}
	}
	section {
		min-height: 80vh;
	}
	footer {
		height: 13vh;
		border-top: 2px solid rgb(234, 234, 234);
		margin-top: 10vh;
		background-color: rgb(214, 214, 214);
		i:hover {
			color: var(--secondary-color);
		}
		.social-links {
			width: 20vw;
			padding: 1vh 2vw 1vh 2vw;
			background-color: rgba(255, 255, 255, 0);
			border-bottom: 1px solid rgb(194, 194, 194);
		}
	}
</style>
