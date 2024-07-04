<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import * as Table from '$lib/components/ui/table';

	const rents = [
		{
			rentId: 'RNT001',
			status: 'Kembali',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 1'
		},
		{
			rentId: 'RNT002',
			status: 'Dipinjam',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 2'
		},
		{
			rentId: 'RNT003',
			status: 'Hilang',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 3'
		},
		{
			rentId: 'RNT004',
			status: 'Kembali',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 1'
		},
		{
			rentId: 'RNT005',
			status: 'Kembali',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 2'
		},
		{
			rentId: 'RNT006',
			status: 'Dipinjam',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 3'
		},
		{
			rentId: 'RNT007',
			status: 'Hilang',
			name: 'User',
			startAt: new Date().toLocaleDateString(),
			endAt: new Date(new Date().setDate(new Date().getDate() + 7)).toLocaleDateString(),
			title: 'Book 1'
		}
	];
</script>

<svelte:head>
	<title>Peminjaman - PustakaDesa</title>
</svelte:head>

<div class="flex-1 space-y-3">
	<div class="flex items-center justify-between gap-5">
		<h1 class="text-2xl font-medium">Peminjaman</h1>
		<div class="flex items-center justify-between gap-3">
			<Button size="sm">Pinjam</Button>
			<Button size="sm">Kembali</Button>
		</div>
	</div>
	<div class="rounded-md border">
		<Table.Root class="">
			<Table.Header>
				<Table.Row>
					<Table.Head class="w-[100px]">ID</Table.Head>
					<Table.Head>Judul</Table.Head>
					<Table.Head>Nama Peminjam</Table.Head>
					<Table.Head>Tanggal Pinjam/Kembali</Table.Head>
					<Table.Head>Status</Table.Head>
					<Table.Head class="text-right">Aksi</Table.Head>
				</Table.Row>
			</Table.Header>
			<Table.Body>
				{#each rents as rent, i (i)}
					<Table.Row>
						<Table.Cell class="font-medium">{rent.rentId}</Table.Cell>
						<Table.Cell>{rent.title}</Table.Cell>
						<Table.Cell>{rent.name}</Table.Cell>
						<Table.Cell>{rent.startAt} - {rent.endAt}</Table.Cell>
						<Table.Cell>{rent.status}</Table.Cell>
						<Table.Cell class="text-right">
							<Button size="sm">Aksi</Button>
						</Table.Cell>
					</Table.Row>
				{/each}
			</Table.Body>
		</Table.Root>
	</div>
</div>
