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

<nav>
	<div id="logo_div">
		<img id="logo" src="/logo.webp" alt="" />
		<h2 class="text-2xl">Soty Ltd.</h2>
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
		<li><a href="/contact">Contact Us</a></li>

		<div class="signup_a"><li><a href="/sign-up">Sign Up</a></li></div>
	</ul>
</nav>
<!-- Navigation Bar for Mobile Dvices -->
<div class="mobile_nav" style="display: {nav};">
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
		<div class="signup_a"><li><a href="/sign-up">Sign Up</a></li></div>
	</ul>
</div>
