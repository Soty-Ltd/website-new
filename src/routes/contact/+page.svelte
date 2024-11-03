<script>
	import SEO from '$lib/components/SEO.svelte';
	import NAV from '$lib/components/NAV.svelte';
</script>

<NAV />
<SEO
	title={'Contact Us |'}
	description={"Get in touch with Soty Ltd. for reliable customer support and assistance. Contact us via phone, email, or visit our office. We're here to help with any inquiries or concerns you may have. Call us today!"}
	image={'s'}
/>

<main class="flex flex-col items-center justify-center w-screen h-max p-8 py-20 max-sm:h-max">
	<div class="flex items-center justify-between max-sm:flex-col">
		<div class="w-1/2 m-3 max-sm:w-full">
			<h1 class="text-5xl text-left">Contact Us - We're Here to Help</h1>
			<h2 class="text-2xl">Get in Touch with Our Team</h2>
			<p>
				We value your feedback, questions, and any concerns you may have. Our dedicated support team
				is ready to assist you with whatever you need. Whether you're looking for product
				information, need help with an order, or just want to share your thoughts, we’re just a
				message away.
			</p>
		</div>
		<div class="w-[600px] m-3 max-sm:w-full">
			<img src="/office.webp" class="rounded-2xl" alt="Office from Soty Ltd." />
		</div>
	</div>

	<div class="flex justify-between w-full mt-10 max-sm:flex-col max-sm:m-0">
		<div class="bg-[#fafceb] rounded-2xl p-7 m-3 w-1/3 max-sm:mx-0 max-sm:w-full">
			<span class="flex items-center">
				<img src="/icons/mail.svg" class="mr-2" alt="" />
				<h3>Mail</h3>
			</span>
			<span>
				<a href="mailto:info@soty.one">info@soty.one</a>
			</span>
		</div>
		<div class="bg-[#fafceb] rounded-2xl p-7 m-3 w-1/3 max-sm:mx-0 max-sm:w-full">
			<span class="flex items-center">
				<img src="/icons/call.svg" class="mr-2" alt="" />
				<h3>Phone</h3>
			</span>
			<span>
				<a href="tel:+19176249703">+1 917-624-9703</a>
			</span>
		</div>
		<div class="bg-[#fafceb] rounded-2xl p-7 m-3 w-1/3 max-sm:mx-0 max-sm:w-full">
			<span class="flex items-center">
				<img src="/icons/mail-adr.svg" class="mr-2" alt="" />
				<h3>Address</h3>
			</span>
			<span>
				<address>
					Unit 6, Jupiter Court <br /> Orion Business Park North Shields,<br /> NE29 7SN <br /> United
					Kingdom
				</address>
			</span>
		</div>
	</div>
</main>
