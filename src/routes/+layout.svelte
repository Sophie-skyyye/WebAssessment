<script>
    let backgroundImage = "../images/image_2.jpg";

    function changeBackgroundImage(image) {
        backgroundImage = `url('${image}')`;
    }
  
    import { onMount } from 'svelte';

    let imgsURL = "";
    const BASE_URL = `https://api.unsplash.com`;
    const ACCESS_KEY = '3nIPvkJHkQsAzWJu8cdbM95fz8fYLCcsxJMqBF-t_oo'; 

    onMount(async () => {
        try {
            const response = await fetch(`${BASE_URL}/photos/red-convertible-coupe-on-gray-pathway-fmF95zYq_CY?client_id=${ACCESS_KEY}`);
            const data = await response.json();
            imgUrl = data.urls.regular;
        } catch (error) {
            console.error('Error fetching image:', error);
        }
    });

</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital@0;1&display=swap" rel="stylesheet">  <!--To import the Poppins font from google-->
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>
<div class="container" style="background-image: {backgroundImage}">
    <nav>
        <!-- svelte-ignore a11y-missing-attribute -->
        <img src="images/logo.PNG" class="logo" />
        <ul>
            <li on:click={() => changeBackgroundImage("../images/DelSolOpening.png")}><a href="/vxi">VXI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_7.jpg")}><a href="/sir">SIR</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_3.png")}><a href="/s">S</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_5.png")}><a href="/si">SI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_4.2.jpg")}><a href="/esi">ESI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_9.jpg")}><a href="/vti">VTI</a></li>
            <li on:click={() => changeBackgroundImage(imgUrl)}><a href="/S2000">S2000</a></li>
        </ul>
        <a
            href="https://www.crxdelsol.fr/Faq/WorkShop/the_del_Sol_guide_full.pdf"
            class="btn">Service Manual</a>
    </nav>
</div>
<slot />
