<script>
	import SEO from '$lib/components/SEO.svelte';
	function sso() {
		alert('Single Sign On currently not available');
	}

	function signup() {
		window.location.replace('sign-up/next-steps');
	}
</script>

<SEO
	title={'Sign Up |'}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<main>
	<div class="data">
		<a id="back" href="/"
			><svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#000"
				><path d="m313-440 224 224-57 56-320-320 320-320 57 56-224 224h487v80H313Z" /></svg
			> Home</a
		>
		<h1>Sign Up</h1>
		<h3>Start your journey with us right now.</h3>
		<br />
		<!-- SSO Sign in -->
		<button class="sso" on:click={() => sso()}>Sign in with Google</button>
		<button class="sso" on:click={() => sso()}>Sign in with GitHub</button>
		<div class="divider">
			<div class="divide"></div>
			<p>Or</p>
			<div class="divide"></div>
		</div>
		<!-- Sign in per E-Mail -->
		<div>
			<label for="">Email</label>
			<br />
			<input type="text" placeholder="john@doe.com" />
		</div>
		<div style="margin: 10px 0 0 0;">
			<label for="">Password</label>
			<br />
			<input type="password" placeholder="" id="pw" />
		</div>
		<button on:click={() => signup()}>Sign Up</button>
	</div>

	<div class="info"></div>
</main>

<style>
	main {
		display: flex;
		height: 100vh;
		width: 100vw;
		padding: 30px;
		box-sizing: border-box;
	}

	.data {
		width: 40vw;
		padding: 40px;
	}

	.info {
		width: 60vw;
		border-radius: 10px;
		background: url('/signup.webp') center;
		background-size: cover;
	}

	h1 {
		text-align: left;
		font-weight: 600;
		font-size: 2.25rem;
	}

	h3 {
		font-weight: 400;
		font-size: 1.25rem;
	}
	input {
		width: 70%;
		border: 1px solid black;
		background: none;
		border-radius: 5px;
		padding: 10px 20px 10px 15px;
		font-size: 1rem;
		margin: 5px 0 0 0;
	}
	button {
		width: 70%;
		border-radius: 5px;
		padding: 10px 20px 10px 15px;
		font-size: 1rem;
		margin: 15px 0 0 0;
		border: 1px solid black;
		box-sizing: content-box;
	}

	.divider {
		display: flex;
		align-items: center;
		width: calc(70% + 35px);
		box-sizing: content-box;
	}

	.divider p {
		margin: 20px;
	}

	.divide {
		border: 1px solid black;
		width: 100%;
		height: 0px;
	}

	#back {
		display: flex;
		align-items: center;
	}

	.sso {
		background: none;
		color: black;
	}

	.sso:hover {
		background-color: #e1f1a5;
	}

	@media screen and (max-width: 700px) {
		main {
			display: flex;
			justify-content: center;
			align-items: center;
		}

		.info {
			display: none;
		}

		.data {
			width: 100vw;
		}

		button,
		input {
			width: 100%;
			box-sizing: border-box;
		}

		.divider {
			width: 100%;
		}
	}
</style>
