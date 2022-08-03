<script lang="ts">
	import { BarGraph } from '.';
	import { Baritem } from '../baritem';

	let data: number[] = [1, 2, 3, 4, 5];
	let title: string = '헬로 월드';
	let minV: number;
	let maxV: number;
</script>

<div class="bargraph" />

<div class="root">
	<BarGraph {data} title="안녕">
		{#each data as d}
			{d}
		{/each}
	</BarGraph>
</div>

<style lang="scss">
	.root {
		background-color: pink;
		height: 80vh;
		border: solid 2px black;
	}
	/*
	.bargraph {
		width: 700px;
		height: 500px;

		display: flex;

		align-items: flex-end;
		justify-content: space-around;
		text-align: center;
		margin: auto;

		border-bottom: solid 2px rgb(170, 170, 170);
		border-left: solid 2px rgb(170, 170, 170);

		background: repeating-linear-gradient(
			0,
			transparent,
			transparent 9.5%,

			rgba(170, 170, 170, 0.7) 10%
		); 
	}*/
</style>
