<script lang="ts">
	export let H1Text: string;
	export let H2Text: string;
	export let BackgroundImageUrl: string;
	export let MobileBackgroundImageUrl: string;
	export let ButtonText: string;
	export let ButtonTitle: string;
	export let ButtonUrl: string;
</script>

<section
	id="banner"
	class="page-banner HC_text-align-center"
	style="background-image: url('{BackgroundImageUrl}')"
>
	<div style="margin: 0px auto; max-width: 1200px " id="homeBanner">
		<div class="row">
			<div
				class="col-md-11 col-md-offset-1 col-sm-11 col-sm-offset-1 col-xs-10 offset-md-1 offset-sm-1 offset-1"
			>
				<h1 class="VP">{@html H1Text}</h1>
				<h2 class="VP2">{@html H2Text}</h2>
			</div>
		</div>
		<div class="row" style="display: block; flex-wrap: nowrap">
			<div style="height: 60px;">&nbsp;</div>
			<div class="col-md-offset-1 col-sm-offset-1 col-xs-offset-1 offset-md-1 offset-sm-1 offset-1">
				{#if ButtonUrl}
					<a href={ButtonUrl.toLowerCase()} title={ButtonTitle} class="homeMainGetEstimate"
						>{ButtonText}</a
					>
				{/if}
			</div>
			<br />
		</div>
	</div>
</section>

<style lang="scss">
	@media (max-width: 800px) {
		.page-banner {
			background-image: url('{MobileBackgroundImageUrl}') !important;
		}
	}
</style>
