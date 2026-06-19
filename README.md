# Império-Conexões
Site de conexão do Império RP
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Conexão Império RP</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:#000;
    color:white;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;
}

.container{
    width:100%;
    max-width:1000px;
    text-align:center;
}

.logo-area{
    margin-bottom:35px;
}

.logo{
    width:220px;
    max-width:100%;
}

.logo-area h2{
    margin-top:10px;
    color:#3db7ff;
    font-size:28px;
}

h1{
    margin-bottom:25px;
}

.opcoes{
    display:flex;
    gap:20px;
    justify-content:center;
    flex-wrap:wrap;
}

.card{
    background:#111;
    border:2px solid #1d1d1d;
    border-radius:15px;
    width:420px;
    padding:25px;
    transition:.3s;
}

.card:hover{
    border-color:#3db7ff;
    transform:translateY(-5px);
}

.card h2{
    color:#3db7ff;
    margin-bottom:15px;
}

.card p{
    line-height:1.6;
    margin-bottom:20px;
}

.ip{
    background:#050505;
    border:1px solid #222;
    border-radius:10px;
    padding:12px;
    margin-bottom:12px;
}

button{
    margin-left:10px;
    padding:6px 12px;
    border:none;
    border-radius:8px;
    background:#2196f3;
    color:white;
    cursor:pointer;
    font-weight:bold;
}

button:hover{
    background:#42a5f5;
}

footer{
    margin-top:30px;
    color:#888;
    font-size:14px;
}
</style>
</head>
<body>

<div class="container">

    <div class="logo-area">
        <img src="582_Sem_Titulo_20250907123551(1).png" class="logo" alt="Império RP">
        <h2>Conexão via Império</h2>
    </div>

    <h1>Escolha sua conexão</h1>

    <div class="opcoes">

        <div class="card">
            <h2>IPv6</h2>

            <p>
                IPv6 é ideal para quem mora no sudeste e sul brasileiro.
            </p>

            <div class="ip">
                <b>IP:</b>
                <span id="ip6">fifuserver.duckdns.org</span>
                <button onclick="copiar('ip6')">Copiar</button>
            </div>

            <div class="ip">
                <b>Porta:</b>
                <span id="porta6">19132</span>
                <button onclick="copiar('porta6')">Copiar</button>
            </div>
        </div>

        <div class="card">
            <h2>IPv4</h2>

            <p>
                IPv4 é bom para regiões mais distantes, ideal para quem mora no norte, nordeste ou centro-oeste brasileiro (ou fora do Brasil).
            </p>

            <div class="ip">
                <b>IP:</b>
                <span id="ip4">fifuserver.minecraft.party</span>
                <button onclick="copiar('ip4')">Copiar</button>
            </div>

            <div class="ip">
                <b>Porta:</b>
                <span id="porta4">01035</span>
                <button onclick="copiar('porta4')">Copiar</button>
            </div>
        </div>

    </div>

    <footer>
        IMPÉRIO RP © 2026
    </footer>

</div>

<script>
function copiar(id){
    const texto = document.getElementById(id).innerText;

    navigator.clipboard.writeText(texto)
    .then(() => {
        alert("Copiado: " + texto);
    });
}
</script>

</body>
</html>
