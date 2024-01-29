<script lang="ts">
	export let rootStyles: string | null = null;
</script>

<span style={rootStyles}>
	<slot />
</span>

<style>
	span {
		flex-grow: 1;
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}
</style>
