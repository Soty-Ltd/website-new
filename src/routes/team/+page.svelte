<script>
	const employees = [
		{ name: 'Oliver Thorns', id: 'thorns', job: 'Chief Executive Officer', group: 'executive' },
		{
			name: 'Samantha Hartley',
			id: 'hartley',
			job: 'Chief Technology Officer',
			group: 'executive'
		},
		{ name: 'Ethan Brooks', id: 'brooks', job: 'Chief Financial Officer', group: 'executive' },
		{ name: 'Maya Patel', id: 'patel', job: 'Chief Marketing Officer', group: 'executive' },
		{
			name: 'Liam Reed',
			id: 'reed',
			job: 'Head of Cloud Infrastructure',
			group: 'engineering'
		},
		{ name: 'Ava Gomez', id: 'gomez', job: 'Lead Software Engineer', group: 'engineering' },
		{ name: 'Noah Clark', id: 'clark', job: 'Senior DevOps Engineer', group: 'engineering' },
		{
			name: 'Sophia Johnson',
			id: 'johnson',
			job: 'Cloud Solutions Architect',
			group: 'engineering'
		},
		{ name: 'Jackson Lee', id: 'lee', job: 'Director of Customer Success', group: 'support' },
		{
			name: 'Emily Thompson',
			id: 'thompson',
			job: 'Cloud Security Specialist',
			group: 'engineering'
		},
		{ name: 'James Miller', id: 'miller', job: 'Data Scientist', group: 'engineering' },
		{ name: 'Olivia Davis', id: 'davis', job: 'Product Manager', group: 'product' },
		{ name: 'Benjamin Taylor', id: 'taylor', job: 'Technical Support Lead', group: 'support' },
		{ name: 'Charlotte Wilson', id: 'wilson', job: 'UX/UI Designer', group: 'design' },
		{
			name: 'Michael Anderson',
			id: 'anderson',
			job: 'Cloud Systems Administrator',
			group: 'engineering'
		},
		{ name: 'Isabella Martinez', id: 'martinez', job: 'Sales Manager', group: 'sales' },
		{ name: 'Alexander King', id: 'king', job: 'Business Development Executive', group: 'sales' },
		{ name: 'Amelia White', id: 'white', job: 'QA Engineer', group: 'engineering' },
		{ name: 'Lucas Brown', id: 'brown', job: 'Network Engineer', group: 'engineering' },
		{ name: 'Grace Walker', id: 'walker', job: 'HR Manager', group: 'hr' },
		{ name: 'Daniel Evans', id: 'evans', job: 'Marketing Specialist', group: 'marketing' },
		{ name: 'Harper Moore', id: 'moore', job: 'Systems Analyst', group: 'engineering' },
		{ name: 'Ella Harris', id: 'harris', job: 'Administrative Assistant', group: 'admin' },
		{ name: 'Sebastian Lewis', id: 'lewis', job: 'Software Developer', group: 'engineering' },
		{ name: 'Zoe Young', id: 'young', job: 'Customer Support Specialist', group: 'support' }
	];
</script>

<nav>
	<div id="logo_div">
		<img id="logo" src="/logo.webp" alt="" />
		<h2>Soty Ltd.</h2>
	</div>

	<div on:click={() => mobileNav()}>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			height="30px"
			viewBox="0 -960 960 960"
			width="30px"
			class="hamburger"
			fill="#000"
			><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z" /></svg
		>
	</div>

	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/news">News</a></li>
		<li><a href="/team">Team</a></li>

		<div class="signup_a"><li><a href="/sign-up">Sign Up</a></li></div>
	</ul>
</nav>
<main>
	x
	<div style="margin-top: 140px;"></div>
	<h1>Meet Our Amazing Team at Soty Ltd.</h1>
	<p>
		Meet the talented individuals who make Soty possible. From creative thinkers and technical
		wizards to strategic planners and customer advocates, our team is dedicated to delivering
		solutions that make a difference. Every team member plays a crucial role in shaping the
		exceptional experience we provide to our clients.
	</p>
	<section class="employees" aria-label="Team Members">
		{#each employees as employee}
			<article
				class="employee"
				id={employee.id}
				style="background: url('/employees/{employee.id}.png') no-repeat center center; background-size: cover; background-color: #F8CFCF;"
				role="region"
				aria-labelledby="{employee.id}-name"
				itemscope
				itemtype="http://schema.org/Person"
			>
				<div class="employeeInfo">
					<h3 id="{employee.id}-name" itemprop="name">{employee.name}</h3>
					<h4 itemprop="jobTitle">{employee.job}</h4>
				</div>
				<!-- Image is now included in HTML with alt text -->
				<img
					src="/employees/{employee.id}.png"
					alt="{employee.name} - {employee.job} - Soty"
					style="display: none;"
					itemprop="image"
				/>
			</article>
		{/each}
	</section>
	<!-- Call to Action Section -->
	<section aria-label="Join Our Team">
		<h2>Want Your Name on Here?</h2>
		<h3>
			Are you still searching for a job? Become part of a dynamic and innovative team here at Soty!
		</h3>
		<button><a href="/careers">View Job Openings</a></button>
	</section>
</main>

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
	}
	.employeeInfo {
		background-color: #f9fce9;
		width: 90%;
		margin: 20px;
		border-radius: 10px;
		padding: 10px;
		border: 2px solid white;
	}
	.employeeInfo h4 {
		margin: 3px 0 0 0;
	}
</style>
