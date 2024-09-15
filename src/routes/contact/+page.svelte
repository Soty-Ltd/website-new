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

<main>
	<section class="contact">
		<div class="contactUs">
			<h1>Contact Us - We're Here to Help</h1>
			<h2>Get in Touch with Our Team</h2>
			<p>
				We value your feedback, questions, and any concerns you may have. Our dedicated support team
				is ready to assist you with whatever you need. Whether you're looking for product
				information, need help with an order, or just want to share your thoughts, we’re just a
				message away.
			</p>
		</div>
		<img class="office" src="/office.jpg" alt="Soty Ltd. Office" width="600px" />
	</section>
	<section class="contactInfo">
		<div class="contactWay">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
				class="lucide lucide-mail"
				><rect width="20" height="16" x="2" y="4" rx="2" /><path
					d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"
				/></svg
			>
			<h3>Write us an E-Mail</h3>
			<a href="mailto:info@soty.one">info@soty.one</a>
		</div>
		<div class="contactWay" id="middle">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
				class="lucide lucide-phone"
				><path
					d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
				/></svg
			>
			<h3>Call Us</h3>
			<a href="tel:">+1</a>
		</div>
		<div class="contactWay">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
				class="lucide lucide-mailbox"
				><path
					d="M22 17a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V9.5C2 7 4 5 6.5 5H18c2.2 0 4 1.8 4 4v8Z"
				/><polyline points="15,9 18,9 18,11" /><path
					d="M6.5 5C9 5 11 7 11 9.5V17a2 2 0 0 1-2 2"
				/><line x1="6" x2="7" y1="10" y2="10" /></svg
			>
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
	main {
		padding: 0 80px;
		height: 150vh;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}
	.contact {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.contactUs h1 {
		text-align: left;
		font-size: 3rem;
	}
	h2 {
		font-size: 2rem;
	}
	p {
		font-size: 1.25rem;
	}

	.contactUs {
		margin: 0 20px 0 0;
	}
	.office {
		border-radius: 20px;
	}
	.contactInfo {
		display: flex;
		align-items: center;
		justify-content: space-between;
		margin: 40px;
		width: calc(100vw - 160px);
	}

	#middle {
		margin: 10px;
	}
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
