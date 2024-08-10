<div class="heroNews">
	<div style="margin: 30px; ">
		<h2>Newsroom</h2>
		<h1>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h1>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button>Read More</button>
	</div>

	<div class="headingImg"></div>
</div>

<main>
	<div class="news">
		<img src="news/hello.jpg" alt="" /><br />
		<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button>Read More</button>
	</div>
	<div class="news">
		<img src="news/hello.jpg" alt="" /><br />
		<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button>Read More</button>
	</div>
	<div class="news">
		<img src="news/hello.jpg" alt="" /><br />
		<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button>Read More</button>
	</div>
	<div class="news">
		<img src="news/hello.jpg" alt="" /><br />
		<h2>Soty Ltd. Enhances Frankfurt <br /> Datacenter with 15 Gigabit Connection</h2>
		<p>Boosting Performance and Reliability for Enhanced Digital Services</p>
		<button>Read More</button>
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
	}

	.headingImg {
		background: url('news/servers.jpg') center;
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
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, 1fr);
		padding: 30px;
	}

	.news {
		background-color: #f9fce9;
		width: 40vw;
		padding: 20px;
		margin: 0 0 2vw 0;
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

		main {
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
		}

		.news {
			width: 80vw;
			margin: 0 0 20px 0;
		}
	}
</style>
