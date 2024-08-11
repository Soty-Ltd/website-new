<script>
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
</script>

<nav>
	<img src="logo.webp" alt="" width="10%" />
	<ul>
		<li><a href="#">hello</a></li>
	</ul>
</nav>
<section class="hero">
	<h1>We turn your on-premises applications <br /> into a dynamic cloud solution in seconds.</h1>
	<button>Learn More</button>
</section>
<section class="us">
	<h2>
		We are a Company from the United Kingdom <br /> that provides you with the perfect Servers
		<br /> to get you started for your Project
	</h2>
	<img src="northshields.webp" alt="" />
</section>

<section class="offers">
	<h1>What we Offer</h1>
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

	<!-- {#each paragraphs as paragraph, index}
		Use inline style to set random positions within the section
		<div
			class="paragraph"
			style="top: {getRandomPosition(index).x}%; left: {getRandomPosition(index)
				.x}%; position: absolute;"
		>
			{paragraph}
		</div>
	{/each} -->
</section>
<section class="datacenters">
	<h1>All of our Datacenters and <br /> probaly one for you</h1>

	<div class="locations">
		<div>London, UK <br /> {getServerPing()}ms <small>*1</small></div>
		<div>Frankfurt, Germany <br /> {getServerPing()}ms</div>
		<div>New York, USA <br /> {getServerPing()}ms</div>
		<div>Stockholm, Sweden <br /> {getServerPing()}ms</div>
		<div>Tokyo, Japan <br /> {getServerPing()}ms</div>
		<div>Toronto, Canada <br /> {getServerPing()}ms</div>
	</div>
</section>
<section class="prices">
	<h2>Some of our Products</h2>
	<div class="products">
		<div class="product">
			<h2>VPS</h2>
			<h3>Starting at 4.59$</h3>
			<button id="productBTN">-></button>
		</div>
		<div class="product">
			<h2>Storage</h2>
			<h3>Starting at 4.59$</h3>
			<button id="productBTN">-></button>
		</div>
		<div class="product">
			<h2>VPNs</h2>
			<h3>Starting at 4.59$</h3>
			<button id="productBTN">-></button>
		</div>
	</div>
</section>
<section class="data_delivered">
	<div>
		<h2 id="data">We delivered over</h2>
		<h1 id="dataDel">{dataTB.toLocaleString()} Gigabyte</h1>
		<div style="display: flex;">
			<h2 id="data">of Data since you opened our Website</h2>
			<small>*2</small>
		</div>
	</div>
</section>
