<script lang="ts">
	import { onMount } from 'svelte';

	export let CountryName = 'Italy';
	export let CountryNameAlternative = 'Italy';
	export let Show3rdLevel = true;

	onMount(() => {
		const script = document.createElement('script');
		script.type = 'application/ld+json';
		script.innerHTML = JSON.stringify({
			'@context': 'https://schema.org',
			'@type': 'BreadcrumbList',
			itemListElement: [
				{
					'@type': 'ListItem',
					position: 1,
					name: 'Secureship',
					item: window.location.origin
				},
				{
					'@type': 'ListItem',
					position: 2,
					name: 'Guides',
					item: `${window.location.origin}/shipping`
				},
				...(Show3rdLevel
					? [
							{
								'@type': 'ListItem',
								position: 3,
								name: 'Canada to ${CountryNameAlternative}',
								item: `${
									window.location.origin
								}/shipping/canada-to-${CountryName.toLowerCase().replace(' ', '-')}`
							}
					  ]
					: [])
			]
		});
		document.body.appendChild(script);
	});
</script>

<section class="bread-crumbs">
	<ol>
		<li>
			<a
				href="/"
				title="Secureship is a Multi-Carrier Business shipping platform that leverages its buying power to get you the best and cheapest prices on shipping"
				>Secureship</a
			>
		</li>
		<li>
			<span>></span><a
				href="/shipping"
				title="International Shipping Guides for countries all over the world">Guides</a
			>
		</li>

		{#if Show3rdLevel}
			<li>
				<span>></span>
				<a
					href="/shipping/canada-to-${CountryName.toLowerCase().replace(' ', '-')}"
					title="Find the best and cheapest way to ship to ${CountryNameAlternative} from Canada"
					>Shipping to ${CountryNameAlternative} from Canada</a
				>
			</li>
		{/if}
	</ol>
</section>
