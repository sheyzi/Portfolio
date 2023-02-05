<script lang="ts">
	export let name: string;
	export let description: string;
	export let department: string;

	export let video: string;

	export let url: string;
</script>

<div
	class="flex gap-[1.5em] md:gap-0 flex-col md:flex-row w-full pt-10 border-t-[6px] border-black justify-between"
>
	<div class="flex flex-col gap-4 justify-between">
		<a href={url}><h2 class="md:text-5xl text-3xl">{name}</h2></a>
		<div class="md:text-2xl md:ml-0 ml-auto text-xl w-[300px] flex flex-col gap-4">
			<p>{description}</p>
			<span class="text-[rgba(43,43,43,.65)]">{department}</span>
		</div>
	</div>
	<div class="md:w-[55%] h-full bg-gray-200 md:p-8 p-4">
		<div class="w-full h-full">
			<a href={url}>
				<video class="w-full h-full" src={video} autoplay />
			</a>
		</div>
	</div>
</div>
