<script>
    var header = document.querySelector("body");
    var vXi = document.getElementById("vxi");
    var sIr = document.getElementById("sir");
    var sI = document.getElementById("si");
    var S = document.getElementById("s");
    var eSi = document.getElementById("esi");
    var vTi = document.getElementById("vti");

    vXi.onclick = function(){
        body.style.backgroundImage = "url(../images/DelSolOpening.png)";
    }
    sIr.onclick = function(){
        body.style.backgroundImage = "url(../images/image_2.jpeg)";
    }
    sI.onclick = function(){
        body.style.backgroundImage = "url(../images/image_3.png)";
    }
    S.onclick = function(){
        body.style.backgroundImage = "url(../images/image_4.1.jpeg)";
    }
    eSi.onclick = function(){
        body.style.backgroundImage = "url(../images/image_4.2.jpeg)";
    }
    vTi.onclick = function(){
        body.style.backgroundImage = "url(../images/DelSolOpening.png)";
    }
</script>


<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<slot />
