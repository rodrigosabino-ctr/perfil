<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Perfil</title>
  <style>
    :root{
      --bg: #0f1724;
      --card: #0b1220;
      --muted: #94a3b8;
      --accent: #7c3aed;
      --glass: rgba(255,255,255,0.04);
      --max-width: 900px;
    }

    *{box-sizing: border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,var(--bg), #071026 120%);
      color: #e6eef8;
      line-height:1.45;
      padding:2rem 1rem;
      display:flex;
      justify-content:center;
    }

    .container{
      width:100%;
      max-width:var(--max-width);
    }

    header{
      text-align:center;
      margin-bottom:1.25rem;
    }

    header h1{
      font-size:clamp(1.25rem,2.4vw,2.2rem);
      letter-spacing: -0.02em;
    }

    main{
      display:grid;
      grid-template-columns: 1fr;
      gap:1rem;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent 30%);
      padding:1.25rem;
      border-radius:16px;
      box-shadow: 0 6px 30px rgba(2,6,23,0.6);
      border:1px solid rgba(255,255,255,0.03);
    }

    section{
      background: var(--card);
      padding:1rem;
      border-radius:12px;
      border:1px solid rgba(255,255,255,0.02);
      transition:transform .18s ease, box-shadow .18s ease;
    }

    section:hover{
      transform:translateY(-6px);
      box-shadow:0 20px 40px rgba(2,6,23,0.6);
    }

    section h2{
      font-size:1.05rem;
      margin-bottom:0.6rem;
      color:#f1f5f9;
    }

    section p{
      color:var(--muted);
    }

    /* Foto de perfil */
    .foto-perfil {
      width: 160px;
      height: 160px;
      object-fit: cover;
      border-radius: 50%;
      border: 3px solid var(--accent);
      box-shadow: 0 6px 20px rgba(0,0,0,0.4);
      transition: transform .2s ease;
    }

    .foto-perfil:hover {
      transform: scale(1.05);
    }

    
    #sobre {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 1rem;
    }

    #sobre .texto {
      max-width: 500px;
    }

    @media(min-width:768px){
      #sobre {
        flex-direction: row;
        text-align: left;
        align-items: center;
      }
      #sobre .texto {
        flex: 1;
      }
    }

    /* Skills */
    #skills ul{
      display:flex;
      flex-wrap:wrap;
      gap:0.5rem;
      list-style:none;
    }

    #skills li{
      padding:0.4rem 0.7rem;
      background:var(--glass);
      backdrop-filter: blur(6px);
      border-radius:999px;
      font-size:0.9rem;
      color:#dbeafe;
      border:1px solid rgba(255,255,255,0.03);
      transition:transform .18s ease, box-shadow .18s ease;
    }

    #skills li:hover{
      transform:translateY(-4px);
      box-shadow:0 6px 18px rgba(0,0,0,0.45);
    }

    /* Links */
    a[href^="mailto:"]{
      color:var(--accent);
      text-decoration:none;
      font-weight:600;
    }

    a[href^="mailto:"]:hover{filter:brightness(1.1)}

    footer{
      margin-top:1rem;
      text-align:center;
      color:var(--muted);
      font-size:0.9rem;
    }

    @media(min-width:840px){
      main{grid-template-columns: 1fr 320px; align-items:start}
      #sobre{grid-column:1/2}
      #skills,#contato{grid-column:2/3}
    }

    :focus{outline:3px solid rgba(124,58,237,0.18);outline-offset:3px}

    @keyframes floatIn{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
    main, header h1, footer{animation:floatIn .5s ease both}

    body.light{
      --bg:#f7fafc; --card:#ffffff; --muted:#475569; --accent:#6d28d9; --glass: rgba(2,6,23,0.03);
      color:#0f1724;
      background: linear-gradient(180deg,#f8fafc,#eef2ff 120%);
    }

    @media print{
      body{background:#fff;color:#000}
      main,section{box-shadow:none;border:none}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Bem-vindo ao meu perfil</h1>
    </header>

    <main>
      <section id="sobre">
        <img src="https://avatars.githubusercontent.com/u/235570508?s=400&u=744fd3848df4336e69573c14173f8565405a63d6&v=4" alt="Foto de perfil" class="foto-perfil">
        <div class="texto">
          <h2>Sobre mim</h2>
          <p>Estudante de Análise e Desenvolvimento de Sistemas.</p>
        </div>
      </section>

     <div class="sidebar">
        <section id="skills">
          <h2>Skills</h2>
          <ul>
            <li>C++</li>
            <li>Python</li>
            <li>HTML</li>
            <li>CSS</li>
          </ul>
        </section>

        <section id="contato">
          <h2>Contato</h2>
          <p>Email: <a href="mailto:rodrigosaino073@gmail.com">rodrigosaino073@gmail.com</a></p>
        </section>
      </div>
    </main>

    <footer>
      <p>&copy; 2025 Rodrigo Sabino</p>
    </footer>
  </div>
</body>
</html>
