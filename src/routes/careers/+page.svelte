<script>
	import NAV from '$lib/components/NAV.svelte';
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

<NAV />
<main>
	<div class="head p-20 pt-32 flex justify-center items-center flex-col bg-[#fafceb]">
		<h1 class="font-bold text-8xl">We're hiring!</h1>
		<h2>We are looking for passionate people to join us on our mission</h2>
	</div>
	<div class="jobs p-14">
		{#each jobs as job}
			<hr class="border-[0.8px] border-solid border-[#4a5567]" />
			<div class="job">
				<div class="flex items-center justify-between">
					<h3 class="text-2xl font-medium">{job.title}</h3>
					<a
						class="flex justify-center items-center"
						href="mailto:{job.mail}?subject=Job Application: {job.title}&body=Please provide us with a CV"
						><h3 class="text-2xl font-medium" id="apply">Apply</h3>
						<img src="/icons/arrowrighttop.svg" alt="" /></a
					>
				</div>
				<p class="desc mt-1 text-xl text-[#4a5567]">{job.desc}</p>
				<div class="mt-3 flex">
					<div
						class="chip flex items-center rounded-full border-solid border-black border-[1px] px-3 py-1 pr-3 mr-2"
					>
						<img src="/icons/clock.svg" alt="" />
						<h4 class="font-normal">{job.time}</h4>
					</div>
					<div
						class="chip flex items-center rounded-full border-solid border-black border-[1px] px-3 py-1 pr-3"
					>
						<img src="/icons/office.svg" alt="" class="m" />
						<h4 class="font-normal">{job.office}</h4>
					</div>
				</div>
			</div>
		{/each}
		<hr class="border-[0.8px] border-solid border-[#4a5567]" />
	</div>
</main>
