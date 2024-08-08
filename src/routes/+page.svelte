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
</script>

<nav>Learn More</nav>
<section class="hero">
	<h1>We turn your on-premises applications <br /> into a dynamic cloud solution in seconds.</h1>
	<button>Learn More</button>
</section>
<section class="us">
	<h2>
		We are a Company from the United Kingdom <br /> that provides you with the perfect Servers
		<br /> to get you started for your Project
	</h2>
	<img src="northshields.jpg" alt="" />
</section>

<section class="offers">
	<h1>What we Offer</h1>
	{#each paragraphs as paragraph, index}
		<!-- Use inline style to set random positions within the section -->
		<div
			class="paragraph"
			style="top: {getRandomPosition(index).x}%; left: {getRandomPosition(index)
				.x}%; position: absolute;"
		>
			{paragraph}
		</div>
	{/each}
</section>
