<!-- <nav>
	<div id="logo_div">
		<img id="logo" src="/logo.webp" alt="" />
		<h2>Soty Ltd.</h2>
	</div>

	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/news">News</a></li>
		<div class="signup_a"><li><a href="/sign-up">Sign Up</a></li></div>
	</ul>
</nav> -->
<SEO
	title={'News |'}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<div class="heroNews">
	<div style="margin: 30px; ">
		<h2>Newsroom</h2>
		<hr />
		<br />
		<h1>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h1>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button on:click={() => location.replace('/news/article/?article=0')}>Read More</button>
	</div>

	<div class="headingImg"></div>
</div>

<main>
	<div class="grid">
		<div class="news">
			<img src="news/hello.webp" alt="" /><br />
			<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
			<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button on:click={() => location.replace('/news/article/?article=1')}>Read More</button>
		</div>
		<div class="news">
			<img src="news/hello.webp" alt="" /><br />
			<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
			<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button on:click={() => location.replace('/news/article/?article=2')}>Read More</button>
		</div>
		<div class="news">
			<img src="news/hello.webp" alt="" /><br />
			<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
			<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button on:click={() => location.replace('/news/article/?article=3')}>Read More</button>
		</div>
		<div class="news">
			<img src="news/hello.webp" alt="" /><br />
			<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
			<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
			<button on:click={() => location.replace('/news/article/?article=4')}>Read More</button>
		</div>
	</div>
</main>

<style>
	* {
		margin: 0;
		padding: 0;
	}
	.heroNews {
		width: 100vw;
		height: max-content;
		background-color: #f9fce9;
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 30px 0 0 0;
	}

	.headingImg {
		background: url('/news/servers.webp') center;
		background-size: cover;
		height: 80vh;
		width: 50vw;
	}
	h1 {
		text-align: left;
	}

	h2 {
		font-weight: bolder;
	}

	p {
		font-size: 1.25rem;
	}

	button {
		border: 1px solid black;
		background: none;
		color: black;
		padding: 10px;
		margin: 10px 0 0 0;
		border-radius: 100px;
	}
	button:hover {
		background-color: #000;
		color: #fff;
	}

	main {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, 1fr);
	}

	.news {
		background-color: #f9fce9;
		width: 40vw;
		padding: 40px;
		margin: 20px;
		box-sizing: border-box;
	}

	.news img {
		max-width: 100%;
	}

	.news h2 {
		font-size: 2rem;
	}

	@media screen and (max-width: 600px) {
		.heroNews {
			display: block;
			margin: 0px;
		}

		.headingImg {
			width: 100vw;
			height: 60vw;
		}

		.grid {
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
		}

		.news {
			width: 80vw;
			margin: 20px;
		}
	}
</style>
