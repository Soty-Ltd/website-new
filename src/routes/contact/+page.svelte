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

<main class="px-20 h-[150vh] flex items-center justify-center flex-col">
	<section class="contact flex justify-between items-center">
		<div class="contactUs mr-5">
			<h1 class="text-left text-5xl">Contact Us - We're Here to Help</h1>
			<h2 class="text-4xl">Get in Touch with Our Team</h2>
			<p class="text-xl">
				We value your feedback, questions, and any concerns you may have. Our dedicated support team
				is ready to assist you with whatever you need. Whether you're looking for product
				information, need help with an order, or just want to share your thoughts, we’re just a
				message away.
			</p>
		</div>
		<img class="office rounded-3xl" src="/office.jpg" alt="Soty Ltd. Office" width="600px" />
	</section>
	<section class="contactInfo flex items-center justify-between m-10 w-screen">
		<div class="contactWay">
			<img src="/icons/mail.svg" alt="" />
			<h3>Write us an E-Mail</h3>
			<a href="mailto:info@soty.one">info@soty.one</a>
		</div>
		<div class="contactWay m-3">
			<img src="/icons/mail.svg" alt="" />
			<h3>Call Us</h3>
			<a href="tel:">+1</a>
		</div>
		<div class="contactWay">
			<img src="/icons/mail-adr.svg" alt="" />
			<h3>Send us a Letter</h3>
			<address itemscope itemtype="https://schema.org/PostalAddress">
				<span itemprop="streetAddress">Unit 6, Jupiter Court</span><br />
				<span itemprop="addressLocality">Orion Business Park</span><br />
				<span itemprop="addressRegion">North Shields</span>,
				<span itemprop="postalCode">NE29 7SN</span><br />
				<span itemprop="addressCountry">United Kingdom</span>
			</address>
		</div>
	</section>
</main>

<style>
	@media screen and (max-width: 600px) {
		main {
			padding: 0 30px;
			height: 240vh;
		}
		.contact {
			flex-direction: column;
			padding: 0 0 0 0;
			justify-content: center;
		}
		.office {
			width: 90vw;
			margin: 20px 0 0 0;
		}
		.contactInfo {
			display: block;
			width: 100%;
		}

		#middle {
			margin: 0;
		}

		.contactWay {
			margin: 20px 0;
		}
	}
	.contactWay {
		background-color: #f9fce9;
		padding: 20px;
		border-radius: 20px;
		width: 90%;
		height: 130px;
	}
</style>
