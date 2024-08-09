<script>
	import { page } from '$app/stores';
</script>

<section class="error">
	<img src="sadhamster.png" alt="" width="150px" />

	<div class="seperator"></div>

	<div style="display: flex; flex-direction:column; align-items:start; margin:25px;">
		<h1>{$page.status} {$page.error.message}</h1>
		<h3>
			{#if (page.status = 404)}
				We couldn't find the page you are looking for, sowwy ):
				<br />
				<button>Go Back Home</button>
			{/if}
		</h3>
	</div>
</section>

<style>
	.error {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	.seperator {
		border: 2px solid black;
		height: 30%;
		margin: 0 0 0 25px;
	}
	button {
		margin: 10px 0 0 0;
	}
</style>
