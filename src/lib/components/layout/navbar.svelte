<script>
	import Button from '../ui/button/button.svelte';
</script>

<nav class="sticky top-0 z-50 border-b bg-background px-5 py-3">
	<div class="container flex max-w-7xl items-center justify-between px-0">
		<a href="/" class="text-xl font-bold">PustakaDesa</a>
		<ul class="flex items-center gap-3">
			<li>
				<Button href="/fitur" variant="ghost">Fitur</Button>
			</li>
			<li>
				<Button href="/masuk" variant="ghost">Masuk</Button>
			</li>
			<li>
				<Button href="/daftar" variant="default">Daftar</Button>
			</li>
		</ul>
	</div>
</nav>
