<script>
	import SEO from '$lib/components/SEO.svelte';
	import NAV from '$lib/components/NAV.svelte';
</script>

<NAV />
<SEO
	title={'Sign Up |'}
	description={'Soty Ltd. - Discover the talented team behind Soty, leaders in cloud computing. Meet our executives, engineers, and support staff who drive innovation and excellence. Learn more about our skilled professionals and their roles.'}
	image={'s'}
/>
<main
	class="flex h-screen w-screen p-8 pt-20 box-border max-sm:flex max-sm:justify-center max-sm:items-center"
>
	<div class="data w-[40vw] p-10 max-sm:w-screen">
		<a id="back" class="flex items-center" href="/"
			><svg
				xmlns="http://www.w3.org/2000/svg"
				height="24px"
				viewBox="0 -960 960 960"
				width="24px"
				fill="#000"
				><path d="m313-440 224 224-57 56-320-320 320-320 57 56-224 224h487v80H313Z" /></svg
			> Home</a
		>
		<h1 class="text-left font-semibold text-4xl">Sign Up</h1>
		<h3 class="font-normal text-xl">Start your journey with us right now.</h3>
		<br />
		<!-- SSO Sign in -->
		<button
			class="sso w-[70%] border-[1px] border-solid border-black bg-transparent rounded-md py-3 pr-5 pl-4 text-base mt-4 box-content text-black hover:bg-[#e1f1a5] max-sm:w-full max-sm:box-border"
			on:click={() => sso()}>Sign in with Google</button
		>

		<button
			class="sso w-[70%] border-[1px] border-solid border-black bg-transparent rounded-md py-3 pr-5 pl-4 text-base mt-4 box-content text-black hover:bg-[#e1f1a5] max-sm:w-full max-sm:box-border"
			on:click={() => sso()}>Sign in with GitHub</button
		>
		<div class="divider flex items-center w-[calc(70%+35px)] box-content max-sm:w-full">
			<div class="divide border-[1px] border-solid border-black w-full h-0"></div>
			<p class="m-5">Or</p>
			<div class="divide border-[1px] border-solid border-black w-full h-0"></div>
		</div>
		<!-- Sign in per E-Mail -->
		<div>
			<label for="">Email</label>
			<br />
			<input
				type="text"
				class="w-[70%] border-[1px] border-solid border-black bg-transparent rounded-md py-3 pr-5 pl-4 text-base mt-1 box-content max-sm:w-full max-sm:box-border"
				placeholder="john@doe.com"
			/>
		</div>
		<div style="margin: 10px 0 0 0;">
			<label for="">Password</label>
			<br />
			<input
				type="password"
				class="w-[70%] border-[1px] border-solid border-black bg-transparent rounded-md py-3 pr-5 pl-4 text-base mt-1 box-content max-sm:w-full max-sm:box-border"
				placeholder="mysafepassword1234"
				id="pw"
			/>
		</div>
		<button
			class="max-sm:w-full max-sm:box-border w-[70%] box-content mt-4 rounded-lg"
			on:click={() => signup()}>Sign Up</button
		>
	</div>

	<div
		class="info w-[60vw] rounded-xl bg-[url('/signup.webp')] bg-center bg-cover max-sm:hidden"
	></div>
</main>
