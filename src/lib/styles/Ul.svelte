<script lang="ts">
	export let className: string;
</script>

<ul class={className}>
	<slot />
</ul>

<style>
	ul {
		list-style-type: none;
		padding: 0;
		margin: 0;
	}
</style>
