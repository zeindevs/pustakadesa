<script lang="ts">
	import { page } from '$app/stores';
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import { Card } from '$lib/components/ui/card';

	$: path = $page.url.pathname;
</script>

<Navbar />

<section id="dashboard" class="relative p-5">
	<div class="container flex max-w-6xl flex-col gap-5 px-0 md:flex-row">
		<div class="w-full md:max-w-[250px] sticky top-20 z-10">
			<Card class="sticky top-20 z-10 w-full bg-background p-3">
				<ul class="flex flex-row gap-2 overflow-x-auto md:flex-col">
					<li>
						<Button
							size="sm"
							href="/dashboard"
							class="w-full justify-between gap-3"
							variant={path === '/dashboard' ? 'default' : 'ghost'}
						>
							Dashboard
						</Button>
					</li>
					<li>
						<Button
							size="sm"
							href="/dashboard/buku"
							class="w-full justify-between gap-3"
							variant={path === '/dashboard/buku' ? 'default' : 'ghost'}>Data Buku</Button
						>
					</li>
					<li>
						<Button
							size="sm"
							href="/dashboard/peminjaman"
							class="w-full justify-between gap-3"
							variant={path === '/dashboard/peminjaman' ? 'default' : 'ghost'}
							>Peminjaman
							<span>0</span>
						</Button>
					</li>
					<li>
						<Button
							size="sm"
							href="/dashboard/member"
							class="w-full justify-between gap-3"
							variant={path === '/dashboard/member' ? 'default' : 'ghost'}>Member</Button
						>
					</li>
					<li>
						<Button
							size="sm"
							href="/dashboard/pengaturan"
							class="w-full justify-between gap-3"
							variant={path === '/dashboard/pengaturan' ? 'default' : 'ghost'}>Pengaturan</Button
						>
					</li>
				</ul>
			</Card>
		</div>
		<slot></slot>
	</div>
</section>

<Footer detail={false} />
