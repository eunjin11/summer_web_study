<script lang="ts">
	//export let text: string;
	export let item: number;
</script>

<div class="baritem" data-number={item} style="height: {item * 100}px;" />

<style lang="scss">
	.baritem {
		text-align: center;

		width: 70px;

		//height: 100px;

		//background: linear-gradient(palegreen, plum);

		background: linear-gradient(palegreen, plum);
	}
</style>
