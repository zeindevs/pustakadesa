<script>
	import { Card, CardContent, CardHeader, CardTitle } from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Dashboard - PustakaDesa</title>
</svelte:head>

<div class="flex-1 space-y-3">
	<h1 class="text-2xl font-medium">Dashboard</h1>
	<div class="grid gap-3 md:grid-cols-2 xl:grid-cols-3">
		<Card>
			<CardHeader class="p-5 pb-3">
				<CardTitle class="text-base font-medium">Total Buku</CardTitle>
			</CardHeader>
			<CardContent class="p-5 pt-0">
				<CardTitle class="text-3xl">0</CardTitle>
			</CardContent>
		</Card>
		<Card>
			<CardHeader class="p-5 pb-3">
				<CardTitle class="text-base font-medium">Peminjaman</CardTitle>
			</CardHeader>
			<CardContent class="p-5 pt-0">
				<CardTitle class="text-3xl">0</CardTitle>
			</CardContent>
		</Card>
		<Card>
			<CardHeader class="p-5 pb-3">
				<CardTitle class="text-base font-medium">Member</CardTitle>
			</CardHeader>
			<CardContent class="p-5 pt-0">
				<CardTitle class="text-3xl">0</CardTitle>
			</CardContent>
		</Card>
	</div>
</div>
