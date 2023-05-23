<script lang="ts">
	export let OverviewTitle = 'Guide to Sending Parcels to Italy';
	export let Paragraph1 =
		"<p>Italy, known for its high fashion and inimitable style, refined cuisine, and fast motor cars is also one of Europe's major industrial and economic powers.</p>";
	export let Paragraph2 =
		'<p>Italians love to shop, and they have readily taken to the internet to buy abroad to the tune of $15.8 billion USD in 2019. And it is expected to grow at 10% per year for the next several years.</p><p>Say, Buon giorno, to doing business in Italy!</p>';
	export let Paragraph3 =
		"<p>Information on this page came from <a href='https://www.adm.gov.it/portale/-/faq-dogane-accise#esp' title='Agenzia delle dogane e dei Monopoli' target='_blank' rel='noopener'>Italian Customs</a> and <a href='https://www.Italy.be/en' title='Taxation and Customs Union' target='_blank' rel='noopener'>European Union</a> sources</p>";
</script>

<section id="overview" class="overview">
	<h2>{OverviewTitle}</h2>
	{@html Paragraph1}
	{@html Paragraph2}
	{@html Paragraph3}
</section>
