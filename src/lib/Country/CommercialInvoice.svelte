<script lang="ts">
	export let CountryName: string;
	export let Phone: string;
	export let Address: string;
	export let CarrierTracking_No: string;
	export let GeneralDescription: string;
	export let InvoiceNumber: string;
	export let CustomsBroker: string;
	export let InvDate: string;
	export let Qty: string;
	export let Description: string;
	export let HTSCode: string | undefined;
	export let CountryOfOrigin: string;
	export let Price: string;
	export let Qty2: string;
	export let Description2: string;
	export let HTSCode2: string | undefined;
	export let CountryOfOrigin2: string;
	export let Price2: string;
	export let TermsofSale: string;
	export let TotalNoPackages: string;
	export let ReasonForExport: string;
	export let ContactName: string;
	export let TotalInvoiceAmount: string;
	export let TotalWeight: string;
	export let TypeOfCI: string;
</script>

<section class="commercial-invoice">
	<h4>Sample Commercial Invoice for {TypeOfCI}</h4>
	<table class="shipinvoice">
		<tr>
			<th>Ship To</th>
			<th>Invoice</th>
		</tr>
		<tr>
			<td>
				{Address}<br /><br />
				<b>Phone: </b>{Phone}
			</td>
			<td>
				<b>Carrier tracking number:</b>
				{CarrierTracking_No}<br />
				<b>General Description:</b><br />
				<span class="highlight">{GeneralDescription}</span><br /><br />
				<b>Invoice number:</b>
				{InvoiceNumber}<br />
				<b>Customs Broker:</b>
				{CustomsBroker}<br />
				<b>Date:</b>
				{InvDate}
			</td>
		</tr>
	</table>
	<table class="line-items">
		<tr>
			<th>QTY</th>
			<th>Description of Goods</th>
			<th>C/O</th>
			<th>SubTotal</th>
		</tr>
		<tr>
			<td>{Qty}</td>
			<td>
				<span class="highlight">{Description}</span><br /><br />
				{#if HTSCode}
					<b>HTS Code:</b> {HTSCode}
				{/if}
			</td>
			<td>{CountryOfOrigin}</td>
			<td>{Price}</td>
		</tr>
		<tr id="lineItem2">
			<td>{Qty2}</td>
			<td>
				<span class="highlight">{Description2}</span><br /><br />
				{#if HTSCode2}
					<b>HTS Code:</b> {HTSCode2}
				{/if}
			</td>
			<td>{CountryOfOrigin2}</td>
			<td>{Price2}</td>
		</tr>
	</table>

	<table class="ci-misc">
		<tr>
			<td>
				<b>Terms of Sale:</b>
				{TermsofSale}<br />
				<b>Total number of packages:</b>
				{TotalNoPackages}<br />
				<b>Reason for export:</b> <span class="highlight">{ReasonForExport}</span><br />
				<b>Contact Name:</b>
				{ContactName}<br />
			</td>
			<td>
				<b>Total Invoice Amount:</b>
				{TotalInvoiceAmount}<br />
				<b>Total Weight:</b>
				{TotalWeight}<br />
			</td>
		</tr>
		<tr>
			<td colspan="2">
				<b>Declaration Statement:</b> I hereby certify that information provided is true and complete
				to the best of my knowledge
			</td>
		</tr>
	</table>
</section>

<style>
	/* Styles for the commercial invoice section */
</style>
