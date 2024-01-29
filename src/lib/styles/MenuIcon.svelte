<script lang="ts">
	export let rtl = false;
	export let rootStyles: string | null = null;
</script>

<span style={rootStyles} class:rtl>
	<slot />
</span>

<style>
	span {
		width: 35px;
		min-width: 35px;
		height: 35px;
		line-height: 35px;
		text-align: center;
		display: inline-block;
		border-radius: 2px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.rtl {
		margin-left: 10px;
	}
	:not(.rtl) {
		margin-right: 10px;
	}
</style>
