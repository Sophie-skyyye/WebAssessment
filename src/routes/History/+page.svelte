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

<div class="crxinfo">
    <p>The Honda CRX, initially launched in 1983, marked the Japanese automaker's foray 
        into the burgeoning market for sport compact cars. This two-seater front-wheel-drive 
        hatchback quickly gained popularity for its agile handling and fuel efficiency, becoming a 
        symbol of the era's burgeoning interest in compact, performance-oriented vehicles. Its first 
        generation, produced until 1987, boasted a lightweight design and a peppy engine, appealing to 
        enthusiasts seeking a blend of nimble handling and practicality. The second generation, introduced 
        in 1988, underwent significant design changes, featuring a more streamlined appearance and enhanced 
        performance capabilities. Its discontinuation in 1991 marked the end of an influential chapter in Honda's history, 
        leaving a lasting legacy as an icon of the brand's commitment to engineering excellence and dynamic driving experiences.</p>
</div>



