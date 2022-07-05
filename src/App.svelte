<script>
	import Map from './Map.svelte';
	export let ready;
</script>

<svelte:head>
	<script defer async
	src="https://maps.googleapis.com/maps/api/js?key=AIzaSyB5HYrOwNUgeMxMWUx3QGp8fev-PWjFoYw&callback=initMap">
	</script>
</svelte:head>

<style>
:global(body) {
	padding: 0;
}
</style>

{ #if ready }
<Map></Map>
{ /if }