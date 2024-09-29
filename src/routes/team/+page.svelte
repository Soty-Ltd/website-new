<script>
	import SEO from '$lib/components/SEO.svelte';
	import NAV from '$lib/components/NAV.svelte';
	const employees = [
		{
			name: 'Oliver Thorns',
			id: 'thorns',
			job: 'Chief Executive Officer',
			group: 'executive',
			color: '#F8CFCF'
		},
		{
			name: 'Samantha Hartley',
			id: 'hartley',
			job: 'Chief Technology Officer',
			group: 'executive',
			color: '#EACFF8'
		},
		{
			name: 'Ethan Brooks',
			id: 'brooks',
			job: 'Chief Financial Officer',
			group: 'executive',
			color: '#CFDAF8'
		},
		{
			name: 'Maya Patel',
			id: 'patel',
			job: 'Chief Marketing Officer',
			group: 'executive',
			color: '#CFF8DF'
		},
		{
			name: 'Liam Reed',
			id: 'reed',
			job: 'Head of Cloud Infrastructure',
			group: 'engineering',
			color: '#F8CFCF'
		},
		{
			name: 'Ava Gomez',
			id: 'gomez',
			job: 'Lead Software Engineer',
			group: 'engineering',
			color: '#EACFF8'
		},
		{
			name: 'Noah Clark',
			id: 'clark',
			job: 'Senior DevOps Engineer',
			group: 'engineering',
			color: '#CFDAF8'
		},
		{
			name: 'Sophia Johnson',
			id: 'johnson',
			job: 'Cloud Solutions Architect',
			group: 'engineering',
			color: '#CFF8DF'
		},
		{
			name: 'Jackson Lee',
			id: 'lee',
			job: 'Director of Customer Success',
			group: 'support',
			color: '#F8CFCF'
		},
		{
			name: 'Emily Thompson',
			id: 'thompson',
			job: 'Cloud Security Specialist',
			group: 'engineering',
			color: '#EACFF8'
		},
		{
			name: 'James Miller',
			id: 'miller',
			job: 'Data Scientist',
			group: 'engineering',
			color: '#CFDAF8'
		},
		{
			name: 'Olivia Davis',
			id: 'davis',
			job: 'Product Manager',
			group: 'product',
			color: '#CFF8DF'
		},
		{
			name: 'Benjamin Taylor',
			id: 'taylor',
			job: 'Technical Support Lead',
			group: 'support',
			color: '#F8CFCF'
		},
		{
			name: 'Charlotte Wilson',
			id: 'wilson',
			job: 'UX/UI Designer',
			group: 'design',
			color: '#EACFF8'
		},
		{
			name: 'Michael Anderson',
			id: 'anderson',
			job: 'Cloud Systems Administrator',
			group: 'engineering',
			color: '#CFDAF8'
		},
		{
			name: 'Isabella Martinez',
			id: 'martinez',
			job: 'Sales Manager',
			group: 'sales',
			color: '#CFF8DF'
		},
		{
			name: 'Alexander King',
			id: 'king',
			job: 'Business Development Executive',
			group: 'sales',
			color: '#F8CFCF'
		},
		{
			name: 'Amelia White',
			id: 'white',
			job: 'QA Engineer',
			group: 'engineering',
			color: '#EACFF8'
		},
		{
			name: 'Lucas Brown',
			id: 'brown',
			job: 'Network Engineer',
			group: 'engineering',
			color: '#CFDAF8'
		},
		{ name: 'Grace Walker', id: 'walker', job: 'HR Manager', group: 'hr', color: '#CFF8DF' },
		{
			name: 'Daniel Evans',
			id: 'evans',
			job: 'Marketing Specialist',
			group: 'marketing',
			color: '#F8CFCF'
		},
		{
			name: 'Harper Moore',
			id: 'moore',
			job: 'Systems Analyst',
			group: 'engineering',
			color: '#EACFF8'
		},
		{
			name: 'Ella Harris',
			id: 'harris',
			job: 'Administrative Assistant',
			group: 'admin',
			color: '#CFDAF8'
		},
		{
			name: 'Sebastian Lewis',
			id: 'lewis',
			job: 'Software Developer',
			group: 'engineering',
			color: '#CFF8DF'
		},
		{
			name: 'Zoe Young',
			id: 'young',
			job: 'Customer Support Specialist',
			group: 'support',
			color: '#F8CFCF'
		},
		{
			name: 'Clara Smith',
			id: 'smith',
			job: 'Software Engineer',
			group: 'support',
			color: '#EACFF8'
		},
		{
			name: 'Emilia Jones',
			id: 'jones',
			job: 'Software Engineer',
			group: 'support',
			color: '#CFF8DF'
		}
	];
</script>

<SEO
	title={'Team and Employees |'}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<NAV />
<main class="flex justify-center items-start flex-col px-12">
	x
	<div style="margin-top: 20vw;"></div>
	<h1>Meet Our Amazing Team at Soty Ltd.</h1>
	<p>
		Meet the talented individuals who make Soty possible. From creative thinkers and technical
		wizards to strategic planners and customer advocates, our team is dedicated to delivering
		solutions that make a difference. Every team member plays a crucial role in shaping the
		exceptional experience we provide to our clients.
		<!-- </p> -->
		<!-- style="background: url('/employees/{employee.id}.png') no-repeat center center; background-size: cover; " -->
	</p>
	<section
		class="employees w-full grid grid-cols-[repeat(auto-fill,minmax(230px,1fr))] grid-rows-[repeat(auto-fill,minmax(340px,300px)] gap-3 my-12 justify-start justify-items-start max-sm:flex max-sm:w-full max-sm:justify-center max-sm:items-center max-sm:flex-col"
		aria-label="Team Members"
	>
		{#each employees as employee}
			<article
				class="employee w-[230px] h-[340px] bg-contain bg-center flex justify-center items-end relative overflow-hidden"
				id={employee.id}
				role="region"
				aria-labelledby="{employee.id}-name"
				itemscope
				style="background-color: {employee.color};"
				itemtype="http://schema.org/Person"
			>
				<div
					class="employeeInfo bg-[#f9fce9] w-[90%] m-5 rounded-[10px] p-3 border-2 border-solid border-white z-50 absolute"
				>
					<h3 id="{employee.id}-name" class="font-medium text-xl" itemprop="name">
						{employee.name}
					</h3>
					<h4 itemprop="jobTitle" class="font-normal mt-1">{employee.job}</h4>
				</div>
				<!-- Image is now included in HTML with alt text -->
				<img
					src="/employees/{employee.id}.png"
					alt="{employee.name} - {employee.job} at Soty Ltd."
					itemprop="image"
					class="employeeImg w-[230px]"
				/>
			</article>
		{/each}
	</section>

	<section
		aria-label="Join Our Team"
		class="job w-full flex flex-col justify-center items-center my-20"
	>
		<h2 class="text-center text-4xl">Want Your Name on Here?</h2>
		<h3 class="font-medium text-center">
			Are you still searching for a job? <br /> Become part of a dynamic and innovative team here at
			Soty!
		</h3>
		<button class="mt-5"><a href="/careers" class="text-[#f0f8cf]">View Job Openings</a></button>
	</section>
</main>
<section class="quote bg-[#e4f1ad] p-0 flex items-center max-sm:flex-col">
	<img
		class="h-[50vh] mx-13"
		src="/quotes/oliver-thorns-chief-executive-officer-soty.png"
		alt="Oliver Thorns | Chief Executive Officer at Soty Ltd."
	/>
	<div class="m-10">
		<img src="/quote.svg" alt="" />
		<h2 class="text-left">
			At Soty Ltd., our people are our greatest asset. We’re committed to building a dynamic and
			inclusive environment where innovation thrives, and every team member feels empowered to drive
			change in the cloud computing industry.
		</h2>
		<div class="quoter mt-1">
			<b class="text-xl">Oliver Thorns</b>
			<p class="text-xl">Chief Executive Officer at Soty Ltd.</p>
		</div>
	</div>
</section>
