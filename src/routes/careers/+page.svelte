<script>
	const jobs = [
		{
			title: 'Cloud Solutions Architect',
			desc: 'Design and implement scalable cloud solutions tailored to client needs, ensuring optimal performance and security.',
			office: 'North Shields, UK',
			time: 'Full Time',
			mail: 'jobs@soty.one'
		},
		{
			title: 'Cloud Infrastructure Engineer',
			desc: 'Manage and optimize cloud infrastructure, focusing on automation, reliability, and efficiency.',
			office: 'North Shields, UK',
			time: 'Full Time',
			mail: 'jobs@soty.one'
		},
		{
			title: 'Full-Stack Developer',
			desc: 'Develop and maintain cloud-based applications, handling both front-end and back-end tasks.',
			office: 'North Shields, UK',
			time: 'Full Time',
			mail: 'jobs@soty.one'
		},
		{
			title: 'DevOps Engineer',
			desc: 'Implement CI/CD pipelines, manage deployments, and ensure seamless cloud operations.',
			office: 'North Shields, UK',
			time: 'Full Time',
			mail: 'jobs@soty.one'
		},
		{
			title: 'UI/UX Designer',
			desc: 'Design intuitive and visually appealing user interfaces for cloud-based applications, focusing on user experience.',
			office: 'North Shields, UK',
			time: 'Full Time',
			mail: 'jobs@soty.one'
		}
	];
</script>

<main>
	<div class="head">
		<h1>We're hiring!</h1>
		<h2>We are looking for passionate people to join us on our mission</h2>
	</div>
	<div class="jobs">
		{#each jobs as job}
			<hr />
			<div class="job">
				<div class="line">
					<h3 class="title">{job.title}</h3>
					<a
						href="mailto:{job.mail}?subject=Job Application: {job.title}&body=Please provide us with a CV"
						><h3 class="title" id="apply">Apply</h3>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							height="30px"
							viewBox="0 -960 960 960"
							width="30px"
							fill="#000"><path d="m216-160-56-56 464-464H360v-80h400v400h-80v-264L216-160Z" /></svg
						></a
					>
				</div>
				<p class="desc">{job.desc}</p>
				<div class="info">
					<div class="chip">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							height="24px"
							viewBox="0 -960 960 960"
							width="24px"
							fill="#000"
							><path
								d="m612-292 56-56-148-148v-184h-80v216l172 172ZM480-80q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-400Zm0 320q133 0 226.5-93.5T800-480q0-133-93.5-226.5T480-800q-133 0-226.5 93.5T160-480q0 133 93.5 226.5T480-160Z"
							/></svg
						>
						<h4>{job.time}</h4>
					</div>
					<div class="chip">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							height="24px"
							viewBox="0 -960 960 960"
							width="24px"
							fill="#000"
							><path
								d="M480-480q33 0 56.5-23.5T560-560q0-33-23.5-56.5T480-640q-33 0-56.5 23.5T400-560q0 33 23.5 56.5T480-480Zm0 294q122-112 181-203.5T720-552q0-109-69.5-178.5T480-800q-101 0-170.5 69.5T240-552q0 71 59 162.5T480-186Zm0 106Q319-217 239.5-334.5T160-552q0-150 96.5-239T480-880q127 0 223.5 89T800-552q0 100-79.5 217.5T480-80Zm0-480Z"
							/></svg
						>
						<h4>{job.office}</h4>
					</div>
				</div>
			</div>
		{/each}
		<hr />
	</div>
</main>

<style>
	h1 {
		font-weight: bold;
		font-size: 5.25rem;
	}

	h3 {
		font-weight: 500;
	}

	h4 {
		font-weight: 400;
	}

	p {
		color: #4a5567;
		font-size: 1.25rem;
	}

	.head {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		padding: 100px 10px;
		background-color: #fafceb;
		/* background: url('marek-pavlik-HQGYz4Eazwc-unsplash.jpg') center;
		background-size: cover; */
	}

	.jobs {
		padding: 50px;
	}

	.job .desc {
		margin: 5px 0 0 0;
	}

	.job .title {
		font-size: 1.5rem;
	}

	.line {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	hr {
		border: 0.8px solid #4a5567;
	}

	.info {
		margin: 10px 0 0 0;
		display: flex;
	}

	.chip {
		border: 1px solid black;
		border-radius: 100px;
		padding: 5px 10px;
		margin: 0px 10px 0px 0px;
		display: flex;
		align-items: center;
	}
	.chip svg {
		margin: 0px 4px 0 0;
	}
	a {
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
