<script lang="ts">
	import { BarGraph } from '@src/components/bargraph';
	import { Baritem } from '@src/components/baritem';
	import _ from 'lodash';
	import * as d3 from 'd3';
	import { svg } from 'd3';
	import { updateData, priceData, type PriceUnit } from '@src/store/index';
	import { onMount, onDestroy } from 'svelte';
	let data: number[] = [1, 2, 3, 5, 8];
	let title: string = 'Hello world';



	//export let data: number[];
	//export let title: string;
	//export let guideCount: number = 5;

	let textNumbers: number[] = [1, 2, 3, 4, 5, 6];

	const legend: number = textNumbers.length;

	let minV: number = Math.min(...textNumbers);
	let maxV: number = Math.max(...textNumbers);
	let diff: number;

	let prices: [number, number][] = [];
	let eleContainerWidth: number;
	let eleContainerHeight: number;

	//const d = getData(7);

	onMount(() => {
		//console.log('mounted');
		updateData(7);
	});

	/*
	const line = d3
		.line<[number, number]>()
		.x((d) => d[0] * 10)
		.y((d) => d[1] * 20000 + 100)
		.curve(d3.curveBasis); */

	const line = d3
		.line<[number, number]>()
		.x((d) => (d[0] * eleContainerWidth) / prices.length)
		.y((d) => ((d[1] - minV) * eleContainerHeight) / diff)
		.curve(d3.curveBasis);

	/*
	$:{
		console.log($priceDate);
		prices = $priceData.map((d)=>d.price);
		//max나 min이 변경될 경우
	} //업데이트 하는 기능
	*/

	let path: string|null|undefined; //임시로 let 붙임

	$: {
		prices = _($priceData)
			.map((d, i) => [i, d.price] as [number, number])
			.take(100)
			.value();
		path = line(prices);
		minV = _(prices)
			.map((p) => p[1])
			.min() as number;
		maxV = _(prices)
			.map((p) => p[1])
			.max() as number;
		diff = maxV - minV;
		console.log(prices);
		console.log(eleContainerWidth, eleContainerHeight);

	}
</script>

prices: {prices}
path: {path}


<div bind:clientWidth={eleContainerWidth}
bind:clientHeight={eleContainerHeight}>
	<svg style="width:100%;">
		<path d={path} />
	</svg>
</div>

<!--
<div class="root">
	<div>
		<select
			style="
		position: fixed; display:block; left: 10px; top: 10px;"
		>
			<option>7</option>
			<option>30</option>
			<option>90</option>
		</select>
		<h1
			style="
		position: fixed; display:block; left: 10px; top: 30px;"
		>
			{$priceData.length}
		</h1>
	</div>

	<div>
		<div class="header">
			<div class="name">DENOM</div>
			<div class="timestamp">TIMESTAMP &nbsp;</div>
			<div class="price">PRICE &nbsp;</div>
			<div class="price">MARKETCAP &nbsp;</div>
			<div class="price">DAYVOLUME</div>
		</div>

		<div class="table">
			{#each $priceData as price}
				<div class="item">
					<div class="name">{price.denom}&nbsp;</div>
					<div class="timestamp">{price.timestamp}&nbsp;</div>
					<div class="price">{price.price}&nbsp;</div>
					<div class="price">{price.marketCap}&nbsp;</div>
					<div class="price">{price.dayVolume}</div>
				</div>
			{/each}
		</div>
	</div>
</div>
-->

<!--
<div class="frame">
	<div class="numbers" style="margin-left:-40px; margin-bottom:-5px;">
		{#each leftGuides as item}
			<div class="numbers">{item}</div>
		{/each}
	</div>
	{#each textNumbers as item}
		<Baritem min={minV} max={maxV} value={item} data-number={item} {legend} />
	{/each}
</div>

<Button {text} color="orange" onClick={(value) => {}}/>
-->
<style lang="scss">
	//.root {
	//	display: flex;
	//}
	/*
	.header {
		top: 15%;
		width: 100%;
		display: flex;
		background-color: pink;
		position: sticky;
	}

	.item {
		display: flex;
		//flex-wrap: wrap;
		border-bottom: solid 2px rgb(170, 170, 170);
		border-right: solid 2px rgb(170, 170, 170);
		//text-align: center;
	}

	.name {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
	.timestamp {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
	.price {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
*/
	/*
	.numbers {
		width: 30px;
		display: flex;
		flex-wrap: wrap;
		margin-top: 90%;
		flex-direction: column-reverse;
		//margin-bottom: -10px;
	}

	.frame {
		width: 700px;
		height: 500px;
		//height는 외부에 의존하게 만들기

		//width: 100%;
		//height: 100%;

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
