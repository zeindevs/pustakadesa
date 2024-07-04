<script>
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import * as Card from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Daftar - PustakaDesa</title>
</svelte:head>

<Navbar />

<section id="login" class="px-5 py-12">
	<Card.Root class="mx-auto max-w-md">
		<Card.Header class="pb-0">
			<Card.Title class="text-2xl">Daftar</Card.Title>
			<Card.Description>Silahkan daftar dengan provider yang tersedia berikut.</Card.Description>
		</Card.Header>
		<form class="space-y-5 p-5">
			<div>
				<Button variant="default" class="w-full">Daftar dengan Google</Button>
			</div>
			<div class="flex items-center justify-center gap-1 text-center text-sm">
				<p class="font-muted-foreground">Sudah punya Akun?</p>
				<a href="/daftar" class="font-medium hover:underline">Masuk</a>
			</div>
		</form>
	</Card.Root>
</section>

<Footer />
