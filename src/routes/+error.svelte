<script>
	import { page } from '$app/stores';
	import NAV from '$lib/components/NAV.svelte';
</script>

<NAV />
<section class="error flex justify-center items-center h-screen">
	<img src="/sadhamster.png" class="mr-6" alt="" width="150px" />

	<div class="seperator border-2 border-solid border-black h-1/3 mr-6"></div>

	<div style="display: flex; flex-direction:column; align-items:start; margin:25px;">
		<h1>{$page.status} {$page.error.message}</h1>
		<h3>
			{#if (page.status = 404)}
				We couldn't find the page you are looking for, sowwy ):
				<br />
				<button class="mt-3" on:click={() => location.replace('/')}>Go Back Home</button>
			{/if}
		</h3>
	</div>
</section>
