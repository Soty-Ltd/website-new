<script>
	import { page } from '$app/stores';

	export let title = 'Home | Soty Ltd.';
	export let description = 'Description of your website.';
	export let image = 'https://soty.one/your-logo.png';
</script>

<svelte:head>
	<title>{title} Soty Ltd.</title>
	<meta name="description" content={description} />
	<meta property="og_site_name" content="soty.one" />
	<meta property="og:url" content="https://www.soty.one{$page.url.pathname.toString()}" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
	<meta property="og:image" content={image} />

	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content="soty.one" />
	<meta property="twitter:url" content="https://www.soty.one{$page.url.pathname.toString()}" />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={description} />
	<meta name="twitter:image" content={image} />
	{@html `  <script type="application/ld+json">{
   "@context": "https://schema.org",
   "@type": "Website",
   "name": "${title} | soty.one,
   "url": "https//www.soty.one${$page.url.pathname}",
   "logo": ${image}  }</script>`}
</svelte:head>
