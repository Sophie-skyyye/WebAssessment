<script>
    let backgroundImage = "../images/image_2.jpg";

    function changeBackgroundImage(image) {
        backgroundImage = `url('${image}')`;
    }
</script>

<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>
<div class="container" style="background-image: {backgroundImage}">
    <nav>
        <!-- svelte-ignore a11y-missing-attribute -->
        <img src="images/logo.PNG" class="logo" />
        <ul>
            <li on:click={() => changeBackgroundImage("../images/DelSolOpening.png")}><a href="/vxi" id="vxi">VXI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_7.jpg")}><a href="/sir" id="sir">SIR</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_3.png")}><a href="/s" id="s">S</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_5.png")}><a href="/si" id="si">SI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_4.2.jpg")}><a href="/esi" id="esi">ESI</a></li>
            <li on:click={() => changeBackgroundImage("../images/image_8.jpg")}><a href="/vti" id="esi">VTI</a></li>
        </ul>
        <a
            href="https://www.crxdelsol.fr/Faq/WorkShop/the_del_Sol_guide_full.pdf"
            class="btn">Service Manual</a>
    </nav>
</div>
<slot />
