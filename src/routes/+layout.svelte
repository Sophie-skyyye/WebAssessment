<script>
    let backgroundImage = "../images/image_2.jpg";

    //Changes the background image of the container element to the specified image.
    function changeBackgroundImage(image) {  //The path to the new background image.
        backgroundImage = `url('${image}')`;
    }
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
            <!-- Changes the background image to "image_7.jpg" when the "SIR" link is clicked. -->
            <li on:click={() => changeBackgroundImage("../images/image_7.jpg")}><a href="/sir">SIR</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_3.png")}><a href="/s">S</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_5.png")}><a href="/si">SI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_4.2.jpg")}><a href="/esi">ESI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_9.jpg")}><a href="/vti">VTI</a></li>
            <li on:click={() => changeBackgroundImage("../images/history.png")}><a href="/History">History</a></li>
        </ul>
        <a
            href="https://www.crxdelsol.fr/Faq/WorkShop/the_del_Sol_guide_full.pdf"
            class="btn">Service Manual</a>
    </nav>
</div>
<slot />
