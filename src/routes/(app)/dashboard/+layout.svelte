<script lang="ts">
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import { Card } from '$lib/components/ui/card';
	import * as Tabs from '$lib/components/ui/tabs';

	interface IMenu {
		title: string;
		url: string;
	}

	let menus: IMenu[] = [
		{
			title: 'Dashoard',
			url: '/dashboard'
		},
		{
			title: 'Data Buku',
			url: '/dashboard/buku'
		},
		{
			title: 'Peminjaman',
			url: '/dashboard/peminjaman'
		},
		{
			title: 'Anggota',
			url: '/dashboard/anggota'
		},
		{
			title: 'Pengaturan',
			url: '/dashboard/pengaturan'
		}
	];

	$: path = $page.url.pathname;
</script>

<Navbar />

<section id="dashboard" class="relative p-5">
	<div class="container flex max-w-6xl flex-col gap-5 px-0 md:flex-row">
		<div class="sticky top-20 z-10 w-full md:max-w-[250px]">
			<Tabs.Root value={path} class="sticky top-20 z-10 flex overflow-x-auto md:hidden">
				<Tabs.List class="mx-auto">
					{#each menus as menu}
						<Tabs.Trigger
							value={menu.url}
							class="text-xs data-[state=active]:bg-primary data-[state=active]:text-background sm:text-sm"
							on:click={() => goto(menu.url)}>{menu.title}</Tabs.Trigger
						>
					{/each}
				</Tabs.List>
			</Tabs.Root>
			<Card class="sticky top-20 z-10 hidden w-full bg-background p-3 md:block">
				<ul class="flex flex-row gap-2 overflow-x-auto md:flex-col">
					{#each menus as menu}
						<li>
							<Button
								size="sm"
								href={menu.url}
								class="w-full justify-between gap-3"
								variant={path === menu.url ? 'default' : 'ghost'}
							>
								{menu.title}
							</Button>
						</li>
					{/each}
				</ul>
			</Card>
		</div>
		<slot></slot>
	</div>
</section>

<Footer detail={false} />
