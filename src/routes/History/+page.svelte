<script>   
    import { onMount } from 'svelte';

    let imgs = [];
    const BASE_URL = `https://api.unsplash.com`;
    const ACCESS_KEY = '3nIPvkJHkQsAzWJu8cdbM95fz8fYLCcsxJMqBF-t_oo'; 

    onMount(async () => {
        try {
            const response = await fetch(`${BASE_URL}/photos/a-couple-of-people-standing-on-top-of-a-blue-car-D2lVPuEcAPk?client_id=${ACCESS_KEY}`);
            const data = await response.json();
            imgs = [data]; // Assuming you want to display only one image
        } catch (error) {
            console.error('Error fetching image:', error);
        }
    });
</script>

{#each imgs as img}
    <img src={img.urls.regular} class ="CRX" />
{/each}





