<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>
<nav>
    <!-- svelte-ignore a11y-missing-attribute -->
    <img src="images/logo.PNG" class="logo">
    <ul>
        <li on:click={changeBackground()}><a href="/vxi" id="vxi">VXI</a></li>
        <li><a href="/sir" id="sir">SIR</a></li>
        <li><a href="/s" id="s">S</a></li>
        <li><a href="/si" id="si">SI</a></li>
        <li><a href="/esi" id="esi">ESI</a></li>
        <li><a href="/vti" id="esi">VTI</a></li>
    </ul>
    <a href="https://www.crxdelsol.fr/Faq/WorkShop/the_del_Sol_guide_full.pdf" class="btn">Service Manual</a>
</nav>
<slot />

