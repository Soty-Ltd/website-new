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

	let dataTB = 514518400;

	function addNumber() {
		dataTB = dataTB + 10;
		console.log('hey');
	}

	const interval = setInterval(addNumber, 10);
</script>

<nav>
	<img src="logo.png" alt="" width="10%" />
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
<section class="datacenters">
	<h1>All of our Datacenters and <br /> probaly one for you</h1>
	<div class="locations">
		<div>London, UK <br /> {getServerPing()}ms</div>
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
			<button>-></button>
		</div>
		<div class="product">
			<h2>VPS</h2>
			<h3>Starting at 4.59$</h3>
			<button>-></button>
		</div>
		<div class="product">
			<h2>VPS</h2>
			<h3>Starting at 4.59$</h3>
			<button>-></button>
		</div>
	</div>
</section>
<section class="data_delivered">
	<h2>We delivered over</h2>
	<h1>{dataTB.toLocaleString()} Gigabyte</h1>
	<h2>of Data</h2>
</section>
