<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import * as Table from '$lib/components/ui/table';

	const members = [
		{
			memberId: 'MEM001',
			status: 'Aktif',
			title: 'User 1',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM002',
			status: 'Aktif',
			title: 'User 2',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM003',
			status: 'Aktif',
			title: 'User 4',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM004',
			status: 'Aktif',
			title: 'User 1',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM005',
			status: 'Aktif',
			title: 'User 2',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM006',
			status: 'Aktif',
			title: 'User 4',
			joinAt: new Date().toLocaleDateString()
		},
		{
			memberId: 'MEM007',
			status: 'Aktif',
			title: 'User 1',
			joinAt: new Date().toLocaleDateString()
		}
	];
</script>

<svelte:head>
	<title>Anggota - PustakaDesa</title>
</svelte:head>

<div class="flex-1 space-y-3">
	<div class="flex items-center justify-between gap-5">
		<h1 class="text-2xl font-medium">Anggota</h1>
		<Button size="sm">Tambah</Button>
	</div>
	<div class="rounded-md border">
		<Table.Root class="">
			<Table.Header>
				<Table.Row>
					<Table.Head class="w-[100px]">ID</Table.Head>
					<Table.Head>Nama</Table.Head>
					<Table.Head>Tanggal Gabung</Table.Head>
					<Table.Head>Status</Table.Head>
					<Table.Head class="text-right">Aksi</Table.Head>
				</Table.Row>
			</Table.Header>
			<Table.Body>
				{#each members as member, i (i)}
					<Table.Row>
						<Table.Cell class="font-medium">{member.memberId}</Table.Cell>
						<Table.Cell>{member.title}</Table.Cell>
						<Table.Cell>{member.joinAt}</Table.Cell>
						<Table.Cell>{member.status}</Table.Cell>
						<Table.Cell class="text-right">
							<Button size="sm">Aksi</Button>
						</Table.Cell>
					</Table.Row>
				{/each}
			</Table.Body>
		</Table.Root>
	</div>
</div>
