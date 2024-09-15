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
<main>
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
	<section class="employees" aria-label="Team Members">
		{#each employees as employee}
			<article
				class="employee"
				id={employee.id}
				role="region"
				aria-labelledby="{employee.id}-name"
				itemscope
				style="background-color: {employee.color};"
				itemtype="http://schema.org/Person"
			>
				<div class="employeeInfo">
					<h3 id="{employee.id}-name" class="font-medium text-xl" itemprop="name">
						{employee.name}
					</h3>
					<h4 itemprop="jobTitle">{employee.job}</h4>
				</div>
				<!-- Image is now included in HTML with alt text -->
				<img
					src="/employees/{employee.id}.png"
					alt="{employee.name} - {employee.job} at Soty Ltd."
					itemprop="image"
					class="employeeImg"
				/>
			</article>
		{/each}
	</section>

	<section aria-label="Join Our Team" class="job">
		<h2>Want Your Name on Here?</h2>
		<h3>
			Are you still searching for a job? <br /> Become part of a dynamic and innovative team here at
			Soty!
		</h3>
		<button><a href="/careers">View Job Openings</a></button>
	</section>
</main>
<section class="quote">
	<img
		src="/quotes/oliver-thorns-chief-executive-officer-soty.png"
		alt="Oliver Thorns | Chief Executive Officer at Soty Ltd."
	/>
	<div>
		<img src="/quote.svg" alt="" />
		<h2>
			At Soty Ltd., our people are our greatest asset. We’re committed to building a dynamic and
			inclusive environment where innovation thrives, and every team member feels empowered to drive
			change in the cloud computing industry.
		</h2>
		<div class="quoter">
			<b>Oliver Thorns</b>
			<p>Chief Executive Officer at Soty Ltd.</p>
		</div>
	</div>
</section>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: start;
		flex-direction: column;
		padding: 0 50px 0;
	}

	.employee h4 {
		font-weight: 400;
	}

	.employee h3 {
		font-weight: 500;
	}

	h2 {
		text-align: center;
	}

	p {
		font-size: 1.25rem;
	}

	button a {
		color: #f0f8cf;
	}
	.employees {
		width: 100%;
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
		grid-template-rows: repeat(auto-fill, minmax(340px, 300px));
		gap: 10px;
		margin: 50px 0;
		justify-items: start; /* Aligns the items to the start of each cell */
		justify-content: start; /* Aligns the entire grid to the start (left) */
	}

	.employee {
		width: 230px;
		height: 340px;
		background-size: contain;
		background-position: center;
		display: flex;
		justify-content: center;
		align-items: end;
		position: relative;
		overflow: hidden;
	}
	.employeeInfo {
		background-color: #f9fce9;
		width: 90%;
		margin: 20px;
		border-radius: 10px;
		padding: 10px;
		border: 2px solid white;
		position: absolute;
		z-index: 100;
	}
	.employeeInfo h4 {
		margin: 3px 0 0 0;
	}

	.employeeImg {
		width: 230px;
	}
	@media screen and (max-width: 500px) {
		.employees {
			display: flex;
			width: 100%;
			justify-content: center;
			align-items: center;
			flex-direction: column;
		}
	}

	.job {
		width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin: 70px 0;
	}

	.job h2 {
		font-size: 2.5rem;
	}

	.job h3 {
		font-weight: 500;
		text-align: center;
	}

	.job button {
		margin: 20px 0 0 0;
	}

	/* Quotes Section */
	.quote {
		background-color: #e4f1ad;
		padding: 0;
		display: flex;
		align-items: center;
	}

	.quote h2 {
		text-align: left;
	}

	.quote > div {
		margin: 40px;
	}

	.quote > img {
		height: 50vh;
		margin: 0 50px;
	}

	.quoter {
		margin: 5px 0 0 0;
	}

	.quoter b {
		font-size: 1.25rem;
	}

	.quoter p {
		font-size: 1.25rem;
	}

	@media screen and (max-width: 600px) {
		.quote {
			flex-direction: column;
		}
	}
</style>
