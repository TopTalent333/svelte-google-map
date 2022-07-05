<script>
	 import mapStyles from './map-styles'; // optional
	 import jq from 'jquery';
	let container;
	let map;
	let zoom = 8;
    let center = {lat: -34.397, lng: 150.644};
    
    import { onMount } from 'svelte';
    
	onMount(async () => {
		map = new google.maps.Map(container, {
            zoom,
			center,
			styles: mapStyles // optional
		});


	});


</script>

<style>
.full-screen {
    width: 100vw;
    height: 500px;
}
</style>

<div class="full-screen" id="maparea" bind:this={container}>
</div>

<div>
Location: <input type="text" id="us2-address" style="width: 200px"/>	
Lat.: <input type="text" id="us2-lat"/>
Long.: <input type="text" id="us2-lon"/>
</div>