<script lang="ts">
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import { Card, CardTitle, CardContent } from '$lib/components/ui/card';

	let features: string[] = ['Kelola Buku', 'Cetak Barcode', 'Peminjaman', 'Member'];
</script>

<svelte:head>
	<title
		>PustakaDesa - Sistem Informasi dan Manajemen Perpustakaan Desa, Gratis dan Open Source.</title
	>
</svelte:head>

<Navbar />

<header class="px-5 py-20">
	<div class="container max-w-6xl space-y-5 px-0 text-center">
		<span class="rounded-full bg-secondary px-2.5 py-1 text-xs font-medium">100% Gratis</span>
		<h1 class="text-3xl font-bold capitalize leading-tight md:text-4xl">
			Sistem Informasi dan Manajemen Perpustakaan Desa, Gratis dan Open Source.
		</h1>
		<p class="text-muted-foreground">Kelola perpustakan lebih mudah dan tersedia secara gratis</p>
		<div>
			<Button href="/daftar" variant="default">Coba Sekarang</Button>
		</div>
	</div>
</header>

<section id="features" class="px-5 pb-16">
	<div class="container max-w-6xl space-y-5 px-0 text-center">
		<h2 class="font-medium">Fitur yang tersedia</h2>
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
