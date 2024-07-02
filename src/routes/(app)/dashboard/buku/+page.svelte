<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import * as Table from '$lib/components/ui/table';

	const books = [
		{
			bookId: 'BOK001',
			status: 'Tersedia',
			title: 'Book 1'
		},
		{
			bookId: 'BOK002',
			status: 'Dipinjam',
			title: 'Book 2'
		},
		{
			bookId: 'BOK003',
			status: 'Hilang',
			title: 'Book 3'
		},
		{
			bookId: 'BOK004',
			status: 'Tersedia',
			title: 'Book 4'
		},
		{
			bookId: 'BOK005',
			status: 'Tersedia',
			title: 'Book 5'
		},
		{
			bookId: 'BOK006',
			status: 'Dipinjam',
			title: 'Book 6'
		},
		{
			bookId: 'BOK007',
			status: 'Hilang',
			title: 'Book 7'
		}
	];
</script>

<svelte:head>
	<title>Data Buku - PustakaDesa</title>
</svelte:head>

<div class="flex-1 space-y-3">
	<div class="flex items-center justify-between gap-5">
		<h1 class="text-2xl font-medium">Data Buku</h1>
		<Button size="sm">Tambah</Button>
	</div>
	<div class="rounded-md border">
		<Table.Root class="">
			<Table.Header>
				<Table.Row>
					<Table.Head class="w-[100px]">ID</Table.Head>
					<Table.Head>Judul</Table.Head>
					<Table.Head>Status</Table.Head>
					<Table.Head class="text-right">Aksi</Table.Head>
				</Table.Row>
			</Table.Header>
			<Table.Body>
				{#each books as book, i (i)}
					<Table.Row>
						<Table.Cell class="font-medium">{book.bookId}</Table.Cell>
						<Table.Cell>{book.title}</Table.Cell>
						<Table.Cell>{book.status}</Table.Cell>
						<Table.Cell class="text-right">
							<Button size="sm">Aksi</Button>
						</Table.Cell>
					</Table.Row>
				{/each}
			</Table.Body>
		</Table.Root>
	</div>
</div>
