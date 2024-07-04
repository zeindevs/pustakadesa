<script>
	import * as Card from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Dashboard - PustakaDesa</title>
</svelte:head>

<div class="flex-1 space-y-3">
	<h1 class="text-2xl font-medium">Dashboard</h1>
	<div class="grid gap-3 md:grid-cols-2 xl:grid-cols-3">
		<Card.Root>
			<Card.Header class="p-5 pb-3">
				<Card.Title class="text-base font-medium">Total Buku</Card.Title>
			</Card.Header>
			<Card.Content class="p-5 pt-0">
				<Card.Title class="text-3xl">0</Card.Title>
			</Card.Content>
		</Card.Root>
		<Card.Root>
			<Card.Header class="p-5 pb-3">
				<Card.Title class="text-base font-medium">Peminjaman</Card.Title>
			</Card.Header>
			<Card.Content class="p-5 pt-0">
				<Card.Title class="text-3xl">0</Card.Title>
			</Card.Content>
		</Card.Root>
		<Card.Root>
			<Card.Header class="p-5 pb-3">
				<Card.Title class="text-base font-medium">Anggota</Card.Title>
			</Card.Header>
			<Card.Content class="p-5 pt-0">
				<Card.Title class="text-3xl">0</Card.Title>
			</Card.Content>
		</Card.Root>
	</div>
</div>
