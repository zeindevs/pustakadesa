<script>
	import Button from '../ui/button/button.svelte';
</script>

<nav class="sticky top-0 z-50 border-b bg-background px-5 py-3">
	<div class="container flex max-w-7xl items-center justify-between px-0">
		<a href="/" class="text-xl font-bold">PustakaDesa</a>
		<ul class="flex items-center gap-3">
			<li class="hidden md:flex">
				<Button href="/fitur" variant="ghost">Fitur</Button>
			</li>
			<li class="">
				<Button href="/dashboard" variant="ghost">Dashboard</Button>
			</li>
			<li class="hidden md:flex">
				<Button href="/daftar" variant="ghost">Daftar</Button>
			</li>
			<li class="">
				<Button href="/masuk" variant="default">Masuk</Button>
			</li>
		</ul>
	</div>
</nav>
