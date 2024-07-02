<script lang="ts">
	import { Footer, Navbar } from '$lib/components/layout';
	import { Card, CardTitle, CardContent } from '$lib/components/ui/card';

	let features: string[] = ['Kelola Buku', 'Cetak Barcode', 'Peminjaman', 'Member'];
</script>

<svelte:head>
	<title>Fitur - PustakaDesa</title>
</svelte:head>

<Navbar />

<header class="px-5 py-16">
	<div class="container max-w-6xl space-y-5 px-0 text-center">
		<h1 class="text-3xl font-medium capitalize leading-tight">Fitur</h1>
	</div>
</header>

<section id="features" class="px-5 pb-12">
	<div class="container max-w-6xl space-y-5 px-0 text-center">
		<div class="grid gap-3 divide-x divide-secondary sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
			{#each features as feature}
				<Card class="cursor-pointer bg-primary text-background">
					<CardContent class="p-5">
						<CardTitle class="text-base font-medium">{feature}</CardTitle>
					</CardContent>
				</Card>
			{/each}
		</div>
	</div>
</section>

<Footer />
