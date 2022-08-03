<script lang="ts">
	//export let text: string;
	export let item: number;
	export let min: number;
	export let max: number;
	export let value: number;
	export let legend: number;

	let height: number = value * 20;
	let width: number = 500 / legend;

	//console height: number = ((value-min)/(max-min))*100;
</script>

<div
	class="baritem"
	data-number={item}
	style="height: {height}%;
	width: {width}px"
/>

<style lang="scss">
	.baritem {
		text-align: center;

		//width: 70px;

		//height: 100px;

		//background: linear-gradient(palegreen, plum);

		background: linear-gradient(palegreen, plum);
	}
</style>
