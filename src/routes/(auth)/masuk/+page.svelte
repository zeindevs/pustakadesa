<script>
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import * as Card from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Masuk - PustakaDesa</title>
</svelte:head>

<Navbar />

<section id="login" class="px-5 py-12">
	<Card.Root class="mx-auto max-w-md">
		<Card.Header class="pb-0">
			<Card.Title class="text-2xl">Masuk</Card.Title>
			<Card.Description>Silahkan login dengan provider yang tersedia berikut.</Card.Description>
		</Card.Header>
		<form class="space-y-5 p-5">
			<div>
				<Button variant="default" class="w-full">Masuk dengan Google</Button>
			</div>
			<div class="flex items-center justify-center gap-1 text-center text-sm">
				<p class="font-muted-foreground">Belum punya Akun?</p>
				<a href="/daftar" class="font-medium hover:underline">Daftar</a>
			</div>
		</form>
	</Card.Root>
</section>

<Footer />
