<script>
	import SEO from '$lib/components/SEO.svelte';
	import NAV from '$lib/components/NAV.svelte';
</script>

<NAV />

<SEO
	title={'News |'}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<main class="">
	<div
		class="heroNews w-screen h-max bg-[#f9fce9] flex justify-between items-center p-9 pt-20 pb-20 max-sm:flex-col"
	>
		<div class="">
			<h2>Newsroom</h2>
			<hr />
			<h1 class="text-left">
				Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection
			</h1>
			<p class="mt-2">Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button class="mt-3" on:click={() => location.replace('/news/article/?article=0')}
				>Read More</button
			>
		</div>

		<img
			src="/news/servers.webp"
			class="h-[70vh] w-[50vw] max-sm:w-full max-sm:h-full mt-8"
			alt=""
		/>
	</div>
	<div class="grid p-8">
		<div class="news w-1/3 bg-[#f9fce9] p-8 rounded-xl max-sm:w-full">
			<img src="news/hello.webp" class="w-full" alt="" /><br />
			<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
			<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button class="mt-3" on:click={() => location.replace('/news/article/?article=1')}
				>Read More</button
			>
		</div>
	</div>
</main>
