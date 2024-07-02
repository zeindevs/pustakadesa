<script lang="ts">
	export let detail = true;
</script>

<footer class="bg-background px-5">
	{#if detail === true}
		<div class="container flex max-w-6xl items-center justify-between px-0 py-10">
			<div class="max-w-sm space-y-2">
				<h5 class="text-xl font-bold">PustakaDesa</h5>
				<p class="text-sm">
					Sistem informasi dan manajemen perpustakaan desa, gratis dan open source.
				</p>
			</div>
		</div>
	{/if}
	<div class="container flex flex max-w-6xl items-center justify-center border-t px-0 py-3">
		<small>Copyright &copy; {new Date().getFullYear()} Pustaka Desa.</small>
	</div>
</footer>
