<script>
	let nav = 'none';
	function mobileNav() {
		if (nav == 'none') {
			nav = 'flex';
		} else {
			nav = 'none';
		}
	}
</script>

<nav
	class="w-screen h-16 bg-[#f9fce9] flex items-center justify-between px-8 box-border fixed z-[10000] border-b border-black border-solid"
>
	<div id="logo_div" class="flex items-center flex-row">
		<img id="logo" class="h-8" src="/logo.webp" alt="" />
		<h2 class="text-2xl ml-3">Soty Ltd.</h2>
	</div>

	<div on:click={() => mobileNav()}>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			height="30px"
			viewBox="0 -960 960 960"
			width="30px"
			class="max-sm:block sm:hidden"
			fill="#000"
			><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z" /></svg
		>
	</div>

	<ul class="items-center max-sm:hidden sm:flex">
		<li><a href="/">Home</a></li>
		<li><a href="/news">News</a></li>
		<li><a href="/team">Team</a></li>
		<li><a href="/contact">Contact Us</a></li>

		<div
			class="bg-[#212b0d] border border-solid border-black p-3 rounded-full hover:bg-transparent group"
		>
			<li>
				<a href="/sign-up" class="text-[#f9fce9] hover:text-black group-hover:text-black">Sign Up</a
				>
			</li>
		</div>
	</ul>
</nav>
<!-- Navigation Bar for Mobile Dvices -->
<div
	class="mobile_nav w-screen h-screen bg-[#fafcea] z-[10000] fixed p-10 box-bordern flex-col items-center text-center text-xl"
	style="display: {nav};"
>
	<div on:click={() => mobileNav()}>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			height="40px"
			viewBox="0 -960 960 960"
			width="40px"
			fill="#000"
			><path
				d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"
			/></svg
		>
	</div>

	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/news">News</a></li>
		<li><a href="/team">Team</a></li>
		<li><a href="/contact">Contact Us</a></li>
		<div
			class="signup_a bg-[#212b0d] border border-solid border-black p-3 rounded-full hover:bg-transparent group px-5 py-1"
		>
			<li>
				<a href="/sign-up" class="text-[#f9fce9] hover:text-black group-hover:text-black">Sign Up</a
				>
			</li>
		</div>
	</ul>
</div>
