<script>   
    import { onMount } from 'svelte';

    let crximg = [];
    let hondagen =[];
    const BASE_URL = `https://api.unsplash.com`;
    const ACCESS_KEY = '3nIPvkJHkQsAzWJu8cdbM95fz8fYLCcsxJMqBF-t_oo'; 

    onMount(async () => {
        try {
            const response = await fetch(`${BASE_URL}/photos/a-couple-of-people-standing-on-top-of-a-blue-car-D2lVPuEcAPk?client_id=${ACCESS_KEY}`);
            const data = await response.json();
            crximg = [data]; // Assuming you want to display only one image
        } catch (error) {
            console.error('Error fetching image:', error);
        }

        try {
            const response = await fetch(`${BASE_URL}/photos/p0rzKtxW9vo?client_id=${ACCESS_KEY}`);
            const data = await response.json();
            hondagen = [data]; // Assuming you want to display only one image
        } catch (error) {
            console.error('Error fetching image:', error);
        }

    });
</script>

{#each crximg as img}
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

{#each hondagen as img}
    <img src={img.urls.regular} class ="Hondagen" />
{/each}

<div class="hondageninfo">
    <p>
        The success of the Honda CRX in the 1980s laid the groundwork for the development of the Honda CRX del Sol, 
        which made its debut in 1992. Building upon the CRX's legacy, the CRX del Sol represented a significant evolution 
        in Honda's approach to compact sports cars. With its innovative design, the CRX del Sol featured a unique targa top 
        that could be stowed in the trunk, instantly transforming the coupe into an open-top roadster. This innovative feature 
        offered drivers the flexibility to enjoy both the exhilarating performance of a coupe and the liberating experience of 
        a convertible, all within a single vehicle. Retaining the CRX's nimble handling and fuel-efficient engines, the CRX del 
        Sol further elevated the driving experience by enhancing comfort and refinement, making it a versatile choice for drivers 
        seeking a balance of performance and practicality.

        The CRX del Sol's introduction marked a new era for Honda's compact sports car offerings. The sleek and aerodynamic design, 
        coupled with its versatile targa top, set the CRX del Sol apart in the market. Despite its resemblance to the CRX, the CRX 
        del Sol boasted a more refined interior, improved handling, and a heightened sense of sophistication. Its appeal extended 
        beyond enthusiasts, attracting a broader audience looking for a spirited yet practical driving experience. While the production 
        of the CRX del Sol ceased in 1997, its impact on Honda's lineup endured, solidifying its place as an innovative and memorable 
        addition to the brand's history of engineering excellence and commitment to delivering dynamic and enjoyable driving experiences.
    </p>
</div>


