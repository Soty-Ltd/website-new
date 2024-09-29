<script>
	import SEO from '$lib/components/SEO.svelte';
	import NAV from '$lib/components/NAV.svelte';
	// Array of paragraph texts
	const paragraphs = [
		'Private Cloud',
		'Multi-cloud',
		'Load Balancing',
		'Networking',
		'VPS',
		'APIs',
		'APIs',
		'High Availability',
		'Scalability',
		'Microservices',
		'Public Cloud',
		'Security',
		'Kubernetes',
		'Hybrid Cloud',
		'Automation',
		'Containers',
		'Virtualization',
		'Infrastructure',
		'Backup',
		'Cloud Storage',
		'Content Delivery Network',
		'DevOps',
		'Edge Computing',
		'Deployment'
	];

	// Function to generate random positions for paragraphs
	function getRandomPosition() {
		const x = Math.random() * 90; // Random x position (0-90%)
		const y = Math.random() * 90; // Random y position (0-90%)
		return { x, y };
	}

	function getServerPing() {
		const ping = Math.random() * 30;
		const ping_round = Math.round(ping);
		return ping_round;
	}

	let dataTB = 0;

	function addNumber() {
		dataTB = dataTB + 10;
	}

	const interval = setInterval(addNumber, 10);

	import { onMount } from 'svelte';

	let scrollContainer;
	let scrollContainer1;
	let scrollContainer2;
	onMount(() => {
		const handleScroll = () => {
			const scrollY = window.scrollY;

			if (scrollContainer) {
				if (scrollY > 400) {
					// Start scrolling horizontally only after scrolling down 400px
					scrollContainer.scrollLeft = (scrollY - 800) * 0.2; // Adjust multiplier as needed
					scrollContainer1.scrollLeft = (scrollY - 850) * 0.2; // Adjust multiplier as needed
					scrollContainer2.scrollLeft = (scrollY - 900) * 0.2; // Adjust multiplier as needed
				} else {
					scrollContainer.scrollLeft = 0; // Ensure horizontal scroll is reset when above 400px
					scrollContainer1.scrollLeft = 0; // Ensure horizontal scroll is reset when above 400px
					scrollContainer2.scrollLeft = 0; // Ensure horizontal scroll is reset when above 400px
				}
			}
		};

		window.addEventListener('scroll', handleScroll);

		// Cleanup event listener when component is destroyed
		return () => {
			window.removeEventListener('scroll', handleScroll);
		};
	});

	function signup() {
		window.location.replace('/sign-up');
	}
</script>

<SEO
	title={''}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<NAV />
<section
	class="hero h-screen w-screen flex justify-center place-items-center flex-col bg-cover bg-center bg-[url('/gradient.webp')] bg-no-repeat max-sm:flex max-sm:items-start max-sm:text-left"
>
	<h1 class="m-5 max-sm:text-left">
		We turn your on-premises applications <br /> into a dynamic cloud solution in seconds.
	</h1>
	<button class="text-base scroll-px-8 py-3 max-md:ml-5" on:click={() => signup()}>Sign Up</button>
</section>
<section class="us flex relative content-center p-8 h-3/5 max-sm:h-4/5">
	<h2
		class="font-thin text-6xl leading-normal absolute z-50 top-1/2 -translate-y-1/2 left-[10%] max-sm:text-4xl max-sm:m-5 max-sm:left-0"
	>
		We are a UK-based company offering top-tier servers to kickstart your project.
	</h2>
	<img
		src="northshields.webp"
		class="h-4/5 absolute right-[10%] opacity-60 max-sm:h-4/5 max-sm:left-1/2 max-sm:-translate-x-1/2"
		alt=""
	/>
</section>

<section
	class="offers h-min py-[7rem] flex relative justify-center items-center bg-[#f9fce9] flex-col"
>
	<h1 class="">What we Offer</h1>
	<div class="test1" bind:this={scrollContainer}>
		<h2 style="font-weight: 500;">Cloud Computing Models</h2>
		<h2>Hybrid Cloud</h2>
		<h2>VPS (Virtual Private Server)</h2>
		<h2>Private Cloud</h2>
		<h2>Multi-cloud</h2>
		<h2>Public Cloud</h2>
		<h2 style="font-weight: 500;">Cloud Computing Models</h2>
		<h2>Hybrid Cloud</h2>
		<h2>VPS (Virtual Private Server)</h2>
		<h2>Private Cloud</h2>
		<h2>Multi-cloud</h2>
		<h2>Public Cloud</h2>
	</div>

	<div class="test1" bind:this={scrollContainer1}>
		<h2 style="font-weight: 500;">Cloud Infrastructure and Managment</h2>
		<h2>Cloud Storage</h2>
		<h2>Content Delivery Network (CDN)</h2>
		<h2>Load Balancing</h2>
		<h2>Networking</h2>
		<h2>High Availability</h2>
		<h2>Scalability</h2>
		<h2>Microservices</h2>
		<h2>Kubernetes</h2>
		<h2>Containers</h2>
		<h2>Virtualization</h2>
		<h2>Infrastructure</h2>
		<h2>Backup</h2>
		<h2>Edge Computing</h2>
	</div>

	<div class="test1" bind:this={scrollContainer2}>
		<h2 style="font-weight: 500;">Cloud Services</h2>
		<h2>APIs</h2>
		<h2>Deployment</h2>
		<h2>Security</h2>
		<h2>Automation</h2>
		<h2>DevOps</h2>
		<h2 style="font-weight: 500;">Cloud Services</h2>
		<h2>APIs</h2>
		<h2>Deployment</h2>
		<h2>Security</h2>
		<h2>Automation</h2>
		<h2>DevOps</h2>
		<h2 style="font-weight: 500;">Cloud Services</h2>
		<h2>APIs</h2>
		<h2>Deployment</h2>
		<h2>Security</h2>
		<h2>Automation</h2>
		<h2>DevOps</h2>
	</div>
</section>
<section
	class="datacenters inline-flex items-center justify-center w-screen text-left h-max box-border p-8 max-sm:block max-sm:py-20"
>
	<h1 class="font-black text-left max-sm:mb-8">
		All of our Datacenters and <br /> probaly one for you
	</h1>

	<div
		class="grid grid-rows-2 grid-cols-3 gap-3 m-10 max-sm:w-full max-sm:grid-rows-[repeat(auto, 1fr)] max-sm:grid-rows-[repeat(auto, 1fr)] max-sm:m-0"
	>
		<div>London, UK <br /> {getServerPing()}ms</div>
		<div>Frankfurt, Germany <br /> {getServerPing()}ms</div>
		<div>New York, USA <br /> {getServerPing()}ms</div>
		<div>Stockholm, Sweden <br /> {getServerPing()}ms</div>
		<div>Tokyo, Japan <br /> {getServerPing()}ms</div>
		<div>Toronto, Canada <br /> {getServerPing()}ms</div>
	</div>
</section>
<section class="prices bg-[#e1f1a5] flex justify-center items-center flex-col py-10">
	<h2 class="font-semibold text-5xl">Some of our Products</h2>
	<div class="products flex justify-center items-center max-sm:block w-screen">
		<div class="bg-white m-3 p-10">
			<h2 class="font-medium text-4xl">VPS</h2>
			<h3 class="font-light text-lg">Starting at 4.59$</h3>
			<button
				id="productBTN"
				class="mt-3 border-2 text-black bg-white rounded-full border-black border-solid hover:bg-black hover:text-white"
				>-></button
			>
		</div>
		<div class="bg-white m-3 p-10">
			<h2 class="font-medium text-4xl">Storage</h2>
			<h3 class="font-light text-lg">Starting at 4.59$</h3>
			<button
				id="productBTN"
				class="mt-3 border-2 text-black bg-white rounded-full border-black border-solid hover:bg-black hover:text-white"
				>-></button
			>
		</div>
		<div class="bg-white m-3 p-10">
			<h2 class="font-medium text-4xl">VPNs</h2>
			<h3 class="font-light text-lg">Starting at 4.59$</h3>
			<button
				id="productBTN"
				class="mt-3 border-2 text-black bg-white rounded-full border-black border-solid hover:bg-black hover:text-white"
				>-></button
			>
		</div>
	</div>
</section>
<section class="data_delivered flex items-center justify-center p-10">
	<div>
		<h2 class="text-4xl">We delivered over</h2>
		<h1 class="font-bold text-8xl text-left">{dataTB.toLocaleString()} Gigabyte</h1>
		<div style="display: flex;">
			<h2 class="text-4xl">of Data since you opened our Website</h2>
		</div>
	</div>
</section>
