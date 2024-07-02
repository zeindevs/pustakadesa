<script>
	import { Footer, Navbar } from '$lib/components/layout';
	import { Button } from '$lib/components/ui/button';
	import { Card, CardHeader, CardTitle, CardDescription } from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Daftar - PustakaDesa</title>
</svelte:head>

<Navbar />

<section id="login" class="px-5 py-12">
	<Card class="mx-auto max-w-md">
		<CardHeader>
			<CardTitle class="text-2xl">Daftar</CardTitle>
			<CardDescription>Silahkan daftar dengan provider yang tersedia berikut.</CardDescription>
		</CardHeader>
		<form class="space-y-5 p-5">
			<div>
				<Button variant="default" class="w-full">Daftar dengan Google</Button>
			</div>
			<div class="flex items-center justify-center gap-1 text-center text-sm">
				<p class="font-muted-foreground">Sudah punya Akun?</p>
				<a href="/daftar" class="font-medium hover:underline">Masuk</a>
			</div>
		</form>
	</Card>
</section>

<Footer />
