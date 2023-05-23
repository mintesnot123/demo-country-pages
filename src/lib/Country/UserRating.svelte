<script lang="ts">
	// export let DivLine1: string;
	// export let DivLine2: string;
</script>

<div class="banner-bottom">
	<div class="reviews">
		<div class="maxWidth row">
			<div>
				<span class="d-none d-sm-inline hidden-xs">Secureship </span>Rating:
				<span id="rating" data-rating="4.9">4.9</span>
				<span class="star-rating" id="starRating">
					<i class="fas fa-star" />
					<i class="fas fa-star" />
					<i class="fas fa-star" />
					<i class="fas fa-star" />
					<i class="fas fa-star" />
				</span>
				<a
					title="Secureship Reviews and Testimonials by Google Users"
					target="_blank"
					rel="nofollow noreferrer"
					href="https://www.google.com/search?q=secureship&oq=secureship&aqs=chrome..69i57j69i60l5.1767j0j7&sourceid=chrome&ie=UTF-8#lrd=0x4cce08a58efcbc3d:0xf0163d6908f77cb1,1,,,"
				>
					<span id="reviews">100</span>
					reviews</a
				>
			</div>
			<div>
				<img
					class="carrier-logo"
					src="/images/carriers/purolator-transparent.png"
					alt="Get Purolator discounted shipping for your business"
					title="Get Purolator discounted shipping for your business"
				/>
				<img
					class="carrier-logo"
					src="/images/carriers/ups-transparent.png"
					alt="Cheap shipping through UPS"
					title="Cheap shipping through UPS"
				/>
				<img
					class="carrier-logo"
					src="/images/carriers/fedex-transparent.png"
					alt="Discounted shipping prices with FedEx"
					title="Discounted shipping prices with FedEx"
				/>
				<div class="visible-xs d-sm-none" style="height: 1px;">
					<br />
				</div>
				<img
					class="carrier-logo"
					src="/images/carriers/canpar-transparent.png"
					alt="Best and discounted pricing with Canpar"
					title="Best and discounted pricing with Canpar"
				/>
				<img
					class="carrier-logo"
					src="/images/carriers/canadapost-transparent.png"
					alt="Use your Canada Post account through Secureship"
					title="Use your Canada Post account through Secureship"
				/>
			</div>
		</div>
	</div>
	<div class="shipping-carriers" />
</div>

<style lang="scss">
	.carrier-logo {
		margin: 0px 5px;
		width: auto;
		height: 40px;
	}

	.reviews,
	.review-content {
		text-align: center;
	}

	.carrier-logo-section {
		text-align: center;
	}

	@media (max-width: 600px) {
		.carrier-logo {
			height: 40px;
		}
	}
</style>
