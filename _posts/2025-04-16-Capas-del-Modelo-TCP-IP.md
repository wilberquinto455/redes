---
layout: post # Asegúrate que este layout exista en _layouts/post.html
title: "Capas del modelo TCP/IP: Visión general"
description: "Exploramos cada una de las capas del modelo TCP/IP de forma detallada. Indispensable para estudiantes de CCNA." # Updated description to match title
date: 2025-04-16 13:00:00 -0500
categories: [redes] # Corrected category format
tags: [TCP/IP, redes, CCNA, protocolos, arquitectura de red, capas del modelo TCP/IP]
author: "Tu Nombre" # Replace with actual author name
image: /redes/assets/images/tcp-ip-thumbnail.jpg # Asegúrate que esta ruta sea correcta
# Opcional: Añadir una referencia al CSS específico si no está en el layout general
# css: /assets/css/tcpip-layers.css # Use the updated CSS file name
---

<div class="container post-content-jekyll">

    <div class="hero-post">
        <h1>Capas del modelo TCP/IP</h1>
        </div>

    <article class="post-content">

        <section class="post-section">
            <p>Como se mencionó en el post anterior, el modelo TCP/IP define cómo se comunican los dispositivos en una red actualmente. Además, es un estándar fundamental para el diseño e implementación de redes modernas.</p>
            <p>Este modelo consta de 4 capas, y cada una tiene funciones específicas. Estas capas se comunican entre sí (con las capas superiores e inferiores), formando un sistema de comunicación completo y eficiente. En esta entrada, exploraremos con más detalle cómo funciona cada una de ellas.</p>
            <p>En este punto, me gustaría saber: ¿Conoces cuáles son las capas del modelo TCP/IP y cómo se comunican entre sí? ¿Sabes qué protocolos operan dentro de cada capa?</p>
            <p>👉 No te preocupes si no lo sabes aún. En esta sección te explicaré de manera clara y sencilla el rol de cada capa del modelo TCP/IP, cómo interactúan entre sí y qué protocolos las componen.</p>
        </section>

        <section class="post-section">
            <h2>Capa de Aplicación TCP/IP</h2>

            <div class="analogy-box">
              <div class="analogy-icon">ℹ️</div> <div class="analogy-content">
                <h3>¿Qué es la Capa de Aplicación?</h3>
                <p>Esta es la cuarta capa del modelo de comunicación TCP/IP y se encuentra más cerca del usuario y de los servicios de las aplicaciones. Gracias a esto, el usuario puede interactuar fácilmente con ella.</p>
              </div>
            </div>

            <p>Por ejemplo, si abres un navegador y escribes <code>https://google.com</code> o incluso solo <code>google.com</code>, notarás que aparece un prefijo como <code>http</code> o <code>https</code>. Ese prefijo indica el protocolo que se está utilizando para la comunicación, y es uno de los protocolos que opera en la capa de aplicación. A continuación se describe alguno de los protocolos que operan en la capa de aplicación del modelo TCP/IP.</p>

            <div class="analogy-box">
                <div class="analogy-icon">📜</div> <div class="analogy-content">
                    <h3>¿Qué es un protocolo?</h3>
                    <p>Un protocolo de red se define como un conjunto de normas y procedimientos estandarizados que regulan la transmisión de datos entre dispositivos conectados. Estas reglas especifican cómo se formatean, direccionan, transmiten y reciben los paquetes de información, asegurando que tanto el emisor como el receptor interpreten correctamente los datos.</p>
                    <p>Por ejemplo, el Protocolo de Transferencia de Hipertexto (HTTP) establece cómo un navegador solicita recursos a un servidor web y cómo este responde, utilizando métodos como GET o POST y códigos de estado como 404 o 200.</p>
                </div>
            </div>

            <div class="functions-grid">
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-globe"></i></div> <h4>HTTP/HTTPS</h4>
                <p>Para la transferencia de páginas web.</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-server"></i></div>
                <h4>DNS</h4>
                <p>Traduce nombres de dominio a direcciones IP.</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-envelope"></i></div>
                <h4>SMTP, POP, IMAP</h4>
                <p>Protocolos para envío y recepción de correo.</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-terminal"></i></div>
                <h4>Telnet y SSH</h4>
                <p>Protocolos para acceso remoto a equipos.</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-file-download"></i></div>
                <h4>FTP, TFTP</h4>
                <p>Para transferencia de archivos.</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-network-wired"></i></div>
                <h4>Otros</h4>
                <p>DHCP, LDAP, SNMP, XMPP, IRC, etc.</p>
              </div>
            </div>

            <p>Estos protocolos definen el formato y control necesario para funciones comunes de comunicación en Internet y son usados por los dispositivos de origen y destino durante las sesiones de comunicación.</p>

            <h3>Ejemplos prácticos</h3>

            <div class="example-details-box">
              <div class="example-header">
                <i class="fas fa-laptop-code"></i>
                <h4>Ejemplo práctico de HTTP</h4>
              </div>
              <div class="example-content">
                <p>Cuando escribes "https://google.com" en tu navegador, ocurre lo siguiente:</p>
                <ol class="example-steps">
                  <li>Tu navegador (cliente) genera una solicitud HTTP GET.</li>
                  <li>Esta solicitud viaja desde la capa de aplicación hacia las capas inferiores.</li>
                  <li>Cuando llega al servidor de Google, este procesa la solicitud y envía una respuesta HTTP.</li>
                  <li>La respuesta contiene el código HTML de la página junto con un código de estado (por ejemplo, 200 OK si todo fue exitoso).</li>
                  <li>Tu navegador recibe esta respuesta, interpreta el HTML y muestra la página web.</li>
                </ol>
                <div class="analogy-box">
                  <div class="analogy-icon">🗣️</div>
                  <div class="analogy-content">
                    <h3>Analogía: Pedir en un Restaurante</h3>
                    <p><strong>HTTP es como el idioma que usas para pedir comida:</strong></p>
                    <ul>
                      <li>Tu navegador (cliente) le dice al camarero (protocolo HTTP) "Quiero la página principal" (solicitud GET).</li>
                      <li>El camarero lleva la orden a la cocina (servidor).</li>
                      <li>La cocina prepara el plato (página HTML).</li>
                      <li>El camarero te trae el plato con una nota "¡Aquí tienes!" (respuesta HTTP 200 OK).</li>
                      <li>Tú (navegador) recibes el plato y lo disfrutas (muestras la página).</li>
                    </ul>
                  </div>
                </div>
                <div class="code-example">
                     <h4>Solicitud HTTP (Simplificada)</h4>
                     <pre><code>GET / HTTP/1.1
Host: google.com
User-Agent: Mozilla/5.0
Accept: text/html,application/xhtml+xml</code></pre>
                </div>
              </div>
            </div>

            <div class="example-details-box">
              <div class="example-header">
                <i class="fas fa-server"></i>
                <h4>Ejemplo práctico de DNS</h4>
              </div>
              <div class="example-content">
                <p>Cuando escribes "google.com" sin el "https://":</p>
                <ol class="example-steps">
                  <li>Tu sistema operativo necesita convertir "google.com" (nombre de dominio) a una dirección IP (por ejemplo, 142.250.190.78).</li>
                  <li>Tu computadora envía una consulta DNS a tu servidor DNS configurado.</li>
                  <li>El servidor DNS busca en su caché o consulta a otros servidores DNS.</li>
                  <li>La respuesta DNS regresa con la dirección IP correspondiente.</li>
                  <li>Con esta IP, ahora tu sistema puede establecer una conexión con el servidor de Google.</li>
                </ol>
                 <div class="analogy-box">
                  <div class="analogy-icon">🗺️</div>
                  <div class="analogy-content">
                    <h3>Analogía: La Guía Telefónica de Internet</h3>
                    <p><strong>DNS es como preguntar por una dirección en una oficina de información:</strong></p>
                    <ul>
                      <li>Quieres ir a la "casa de Google" (google.com), pero no sabes la dirección exacta (IP).</li>
                      <li>Preguntas al informador (servidor DNS): "¿Dónde está la casa de Google?".</li>
                      <li>El informador busca en su mapa (caché/base de datos) o pregunta a otros informadores.</li>
                      <li>Te da la dirección: "Está en la calle 142.250.190.78".</li>
                      <li>Ahora ya sabes cómo llegar (puedes iniciar la conexión).</li>
                    </ul>
                  </div>
                </div>
                <p>Es como un directorio telefónico que traduce nombres a números: en lugar de memorizar <code>142.250.190.78</code>, simplemente recordamos "google.com".</p>
              </div>
            </div>

            <p>Estos ejemplos muestran cómo la capa de aplicación proporciona servicios directamente utilizables por los usuarios finales, mientras que las capas inferiores (transporte, red y acceso a la red) se encargan del trabajo "invisible" de mover los datos de manera confiable entre los dispositivos.</p>

            <div class="cta-container">
            <h4>¿Te gustaría profundizar más?</h4>
            <p>Revisa estos recursos adicionales:</p>
            <ul>
             <li><a href="https://docs.google.com/document/d/1xMRlZn9tTpOKSTDwzAEbV4YRyG7acaYD/edit?usp=sharing&ouid=100942887710428516849&rtpof=true&sd=true" target="_blank" rel="noopener noreferrer">¿Qué son los Protocolos?</a></li>
            </ul>
          </div>
            
        </section>

        </article>

    </div>
<style>
/* --- Base Styles & Variables --- */
:root {
    --color-primary: #1e88e5; /* A slightly brighter blue */
    --color-secondary: #43a047; /* A nice green */
    --color-tcp: #3f51b5; /* Indigo for TCP */
    --color-udp: #fb8c00; /* Orange for UDP */
    --color-bg-light: #ffffff;
    --color-bg-medium: #f7f9fc; /* Lighter background for cards */
    --color-bg-dark: #37474f; /* Darker background */
    --color-text: #263238; /* Dark grey for text */
    --color-text-light: #546e7a; /* Lighter grey */
    --color-border: #e0e0e0; /* Softer border color */
    --color-link: var(--color-primary);
    --border-radius: 12px; /* More rounded corners */
    --box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08); /* Softer shadow */
    --box-shadow-hover: 0 6px 20px rgba(0, 0, 0, 0.12);
}

/* Aplica estilos base al contenido generado por Jekyll */
/* Usa una clase específica en el body o div contenedor en tu layout */
.post-content-jekyll {
    font-family: 'Inter', sans-serif;
    line-height: 1.7;
    color: var(--color-text);
}

/* Contenedor principal (si no está en el layout) */
.container {
    max-width: 900px;
    margin: 2rem auto;
    padding: 0 1rem;
}

/* --- Typography --- */
.post-content-jekyll h1,
.post-content-jekyll h2,
.post-content-jekyll h3,
.post-content-jekyll h4 {
    font-weight: 700;
    color: var(--color-text);
    margin-top: 2.5rem;
    margin-bottom: 1.5rem;
}

/* Estilo específico para el H1 del hero */
.hero-post h1 {
    font-size: 3rem;
    margin-bottom: 0.5rem;
    color: white;
    border-bottom: none;
    text-align: center;
}
/* Estilo general para H1 (si aparece en otro lugar) */
 .post-content-jekyll h1:not(.hero-post h1) {
    font-size: 2.8rem;
    color: var(--color-primary);
    text-align: center;
 }


.post-content-jekyll h2 {
    font-size: 2rem;
    border-bottom: 2px solid var(--color-primary);
    padding-bottom: 0.5rem;
    color: var(--color-primary);
}

.post-content-jekyll h3 {
    font-size: 1.5rem;
    color: var(--color-secondary);
}

.post-content-jekyll h4 {
    font-size: 1.2rem;
    color: var(--color-text);
}

.post-content-jekyll p {
    margin-bottom: 1.2rem;
    color: var(--color-text-light);
    font-size: 1.05rem;
}

.post-content-jekyll a {
    color: var(--color-link);
    text-decoration: none;
    transition: color 0.3s ease;
}

.post-content-jekyll a:hover {
    /* CSS 'darken' no existe, usamos un filtro o un color precalculado */
    /* filter: brightness(90%); */
    color: #1565c0; /* Color precalculado más oscuro */
    text-decoration: underline;
}

.post-content-jekyll pre {
    background-color: var(--color-bg-dark);
    color: #f0f0f0;
    padding: 1.5rem;
    border-radius: var(--border-radius);
    overflow-x: auto;
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.95rem;
    line-height: 1.5;
    box-shadow: inset 0 2px 5px rgba(0,0,0,0.2);
    margin-bottom: 1.2rem; /* Añadir margen inferior */
}

/* Estilo para código inline */
.post-content-jekyll :not(pre) > code {
    background-color: #e0e0e0;
    padding: 0.2em 0.4em;
    border-radius: 4px;
    font-size: 0.9em;
    color: var(--color-text);
}

/* Reset para código dentro de pre */
.post-content-jekyll pre code {
    background-color: transparent;
    padding: 0;
    border-radius: 0;
    font-size: inherit;
    color: inherit;
    border: none;
}

/* --- Layout & Sections --- */
.post-section {
    margin-bottom: 3.5rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--color-border);
}
.post-section:last-child {
    border-bottom: none;
    margin-bottom: 0;
}

/* --- Hero Section --- */
.hero-post {
    background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
    color: white;
    padding: 3rem 2rem;
    border-radius: var(--border-radius);
    margin-bottom: 3rem;
    text-align: center;
    box-shadow: var(--box-shadow);
}

/* .hero-post h1 ya está definido arriba */

.hero-post .subtitle {
    font-size: 1.4rem;
    opacity: 0.9;
    font-weight: 400;
    margin-top: 0;
    color: white; /* Asegurar color blanco */
}

/* --- Analogy Box --- */
.analogy-box {
    background-color: var(--color-bg-medium);
    border-left: 5px solid var(--color-secondary);
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 var(--border-radius) var(--border-radius) 0;
    display: flex;
    align-items: flex-start;
    gap: 1rem;
    box-shadow: var(--box-shadow);
}

.analogy-icon {
    font-size: 2rem;
    color: var(--color-secondary);
    line-height: 1;
}

.analogy-content h3 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.3rem;
    color: var(--color-secondary);
}
.analogy-content p {
    margin-bottom: 0.5rem;
    font-size: 1rem;
}
.analogy-content p:last-child {
    margin-bottom: 0;
}

/* --- Functions Grid --- */
.functions-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
}

.function-card {
    background-color: var(--color-bg-light);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    text-align: center;
    box-shadow: var(--box-shadow);
    border: 1px solid var(--color-border);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.function-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--box-shadow-hover);
}

.function-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    display: inline-block;
    background-color: var(--color-primary);
    color: white;
    width: 60px;
    height: 60px;
    line-height: 60px;
    border-radius: 50%;
}

.function-card h3 {
    margin-top: 0;
    margin-bottom: 0.8rem;
    font-size: 1.2rem;
    color: var(--color-primary);
}
.function-card p {
    font-size: 0.95rem;
    margin-bottom: 0;
}

/* --- TCP vs UDP Comparison --- */
.protocol-comparison {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-top: 2rem;
}

.protocol-card {
    background-color: var(--color-bg-light);
    border-radius: var(--border-radius);
    padding: 2rem;
    box-shadow: var(--box-shadow);
    border: 1px solid var(--color-border);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    display: flex; /* Added for vertical alignment */
    flex-direction: column; /* Stack header and content */
}
 .protocol-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--box-shadow-hover);
}


.protocol-header {
    display: flex;
    align-items: center;
    margin-bottom: 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid var(--color-border);
}

.protocol-icon {
    font-size: 2rem;
    margin-right: 1rem;
    width: 50px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    border-radius: 50%;
    color: white;
    flex-shrink: 0; /* Prevent icon shrinking */
}

.protocol-card.tcp .protocol-icon { background-color: var(--color-tcp); }
.protocol-card.udp .protocol-icon { background-color: var(--color-udp); }

.protocol-card h3 {
    margin: 0;
    font-size: 1.4rem;
}
.protocol-card.tcp h3 { color: var(--color-tcp); }
.protocol-card.udp h3 { color: var(--color-udp); }

.protocol-content {
     flex-grow: 1; /* Allow content to fill space */
}

.protocol-content p {
    margin-bottom: 1.5rem;
    font-size: 1rem;
}

.protocol-content h4 {
    font-size: 1.1rem;
    margin-bottom: 0.8rem;
    color: var(--color-text);
}

.feature-list {
    list-style: none;
    padding-left: 0;
    margin-bottom: 1.5rem;
}

.feature-list li {
    margin-bottom: 0.5rem;
    padding-left: 1.5em;
    position: relative;
    font-size: 0.95rem;
}

.feature-list li::before {
    content: '✓'; /* Checkmark */
    position: absolute;
    left: 0;
    color: var(--color-secondary);
    font-weight: bold;
}

.use-cases {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
}

.use-case {
    background-color: var(--color-bg-medium);
    color: var(--color-text-light);
    padding: 0.3rem 0.8rem;
    border-radius: 20px; /* Pill shape */
    font-size: 0.85rem;
    border: 1px solid var(--color-border);
}
.protocol-card.tcp .use-case { border-color: var(--color-tcp); background-color: #e8eaf6; color: var(--color-tcp);}
.protocol-card.udp .use-case { border-color: var(--color-udp); background-color: #fff3e0; color: var(--color-udp);}


/* --- Three-Way Handshake --- */
.handshake-container {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.handshake-step {
    background-color: var(--color-bg-medium);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    display: flex;
    align-items: center;
    gap: 1.5rem;
    box-shadow: var(--box-shadow);
    border: 1px solid var(--color-border);
}

.step-number {
    font-size: 1.5rem;
    font-weight: bold;
    color: white;
    background-color: var(--color-primary);
    min-width: 40px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    border-radius: 50%;
    flex-shrink: 0;
}

.step-devices {
    display: flex;
    align-items: center;
    gap: 1rem;
    min-width: 180px; /* Ensure alignment */
    font-size: 0.9rem;
    text-align: center;
}
 .device {
    font-size: 1.5rem; /* Larger emojis */
 }

.arrow {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.arrow-line {
    font-size: 1.8rem;
    color: var(--color-primary);
    font-weight: bold;
}
.arrow.reverse .arrow-line {
     color: var(--color-secondary);
}

.arrow-label {
    font-size: 0.8rem;
    font-weight: bold;
    color: var(--color-text-light);
    background-color: #e0e0e0;
    padding: 0.1rem 0.4rem;
    border-radius: 4px;
    margin-bottom: 0.2rem; /* Space between label and arrow */
}
.arrow.reverse .arrow-label {
     background-color: #c8e6c9; /* Light green background */
     color: var(--color-secondary);
}


.step-description {
     flex-grow: 1; /* Allow description to take space */
}

.step-description h4 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.1rem;
    color: var(--color-primary);
}
.step-description p {
    margin-bottom: 0;
    font-size: 0.95rem;
}

/* --- Code Example Box --- */
.code-example {
    margin-top: 2rem;
    border: 1px solid var(--color-border);
    border-radius: var(--border-radius);
    overflow: hidden; /* Clip the pre tag */
    box-shadow: var(--box-shadow);
}
.code-example h4 {
     background-color: var(--color-bg-medium);
     margin: 0;
     padding: 0.8rem 1.5rem;
     font-size: 1rem;
     border-bottom: 1px solid var(--color-border);
     color: var(--color-text-light);
}
.code-example pre {
    margin: 0;
    border-radius: 0 0 var(--border-radius) var(--border-radius);
    box-shadow: none; /* Remove inner shadow */
    border: none;
}

/* --- Ports Section --- */
.ports-container {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.ports-group {
    background-color: var(--color-bg-medium);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    border: 1px solid var(--color-border);
}

.ports-group h3 {
    margin-top: 0;
    margin-bottom: 1rem;
    font-size: 1.3rem;
    color: var(--color-primary);
}

.port-examples {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
}

.port-example {
    background-color: var(--color-bg-light);
    padding: 0.8rem 1rem;
    border-radius: var(--border-radius);
    display: flex;
    align-items: center;
    gap: 0.8rem;
    border: 1px solid var(--color-border);
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    min-width: 120px; /* Minimum width for consistency */
}

.port-number {
    font-weight: bold;
    color: var(--color-primary);
    font-size: 1.1rem;
    min-width: 30px; /* Ensure space */
    text-align: right;
}

.port-name {
    font-size: 0.95rem;
    color: var(--color-text);
    flex-grow: 1; /* Take remaining space */
}

.port-icon {
    font-size: 1.3rem;
}

/* --- Interactive Tip / Command Tabs --- */
.interactive-tip {
    background-color: #e3f2fd; /* Light blue background */
    border: 1px solid #90caf9;
    padding: 1.5rem;
    border-radius: var(--border-radius);
    margin-top: 2rem;
}
.interactive-tip h4 {
    margin-top: 0;
    color: var(--color-primary);
    font-size: 1.2rem;
}

.command-tabs {
    display: flex;
    gap: 0.5rem;
    margin-bottom: 1rem;
    border-bottom: 1px solid #90caf9;
}

.command-tab {
    padding: 0.6rem 1.2rem;
    cursor: pointer;
    border-radius: 8px 8px 0 0;
    background-color: #bbdefb; /* Lighter blue for inactive tabs */
    color: var(--color-primary);
    font-weight: bold;
    transition: background-color 0.3s ease;
    border: 1px solid transparent;
    border-bottom: none;
    position: relative;
    bottom: -1px; /* Align with border */
}

.command-tab.active {
    background-color: #e3f2fd; /* Match container background */
    border-color: #90caf9;
    border-bottom-color: #e3f2fd; /* Hide bottom border part */
}

.command-content {
    display: none; /* Hide content by default */
}
.command-content.active {
    display: block; /* Show active content */
}
.command-content pre {
    background-color: var(--color-bg-dark);
    color: #f0f0f0;
    border-radius: 8px; /* Smaller radius inside */
    margin-top: 0;
}
.command-content p { /* Style the small text below pre */
    font-size: 0.9rem;
    color: var(--color-text-light);
    margin-top: -0.5rem; /* Adjust spacing */
    margin-bottom: 1rem;
}
.command-content p small {
    font-size: inherit; /* Inherit size */
}


/* --- Multiplexing --- */
.multiplexing-container {
    display: grid;
    grid-template-columns: 1fr; /* Stack on small screens */
    gap: 2rem;
    margin-top: 2rem;
}

.multiplex-section {
    background-color: var(--color-bg-medium);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    border: 1px solid var(--color-border);
}

.multiplex-section h3 {
    text-align: center;
    margin-top: 0;
    margin-bottom: 1.5rem;
    font-size: 1.3rem;
    color: var(--color-primary);
}

.multiplex-illustration {
    display: flex;
    align-items: center;
    justify-content: space-around;
    gap: 1rem;
    margin-bottom: 1rem;
    text-align: center;
}

.app-container {
    display: flex;
    flex-direction: column;
    gap: 0.8rem;
    align-items: stretch; /* Make apps same width */
}

.app {
    background-color: var(--color-bg-light);
    padding: 0.8rem;
    border-radius: 8px;
    border: 1px solid var(--color-border);
    font-size: 0.9rem;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}
.app small {
    display: block;
    font-size: 0.75rem;
    color: var(--color-text-light);
    margin-top: 0.2rem;
}

.multiplex-arrows {
    font-size: 2rem;
    color: var(--color-primary);
    flex-shrink: 0;
}

.transport-layer, .network {
    background-color: #b3e5fc; /* Light blue */
    padding: 1rem;
    border-radius: var(--border-radius);
    font-weight: bold;
    color: var(--color-primary);
    border: 1px dashed var(--color-primary);
    position: relative;
    min-width: 100px; /* Ensure some width */
    text-align: center; /* Center text */
}
.network {
     background-color: #c8e6c9; /* Light green */
     color: var(--color-secondary);
     border-color: var(--color-secondary);
}

.transport-layer .tag {
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--color-primary);
    color: white;
    padding: 0.2rem 0.5rem;
    border-radius: 4px;
    font-size: 0.7rem;
    white-space: nowrap;
}

.multiplex-section p {
    text-align: center;
    font-size: 0.95rem;
    margin-top: 1.5rem;
    margin-bottom: 0;
}

/* --- Real Example Box --- */
.real-example {
    background-color: #fffde7; /* Light yellow */
    border: 1px solid #fff59d;
    padding: 1.5rem;
    border-radius: var(--border-radius);
    margin-top: 2rem;
}
.real-example h4 {
    margin-top: 0;
    color: #fbc02d; /* Amber */
    font-size: 1.2rem;
}

/* --- Case Study --- */
.case-study-steps {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.case-step {
    display: flex;
    gap: 1.5rem;
    background-color: var(--color-bg-medium);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    border: 1px solid var(--color-border);
    box-shadow: var(--box-shadow);
}
.case-step .step-number {
     background-color: var(--color-secondary); /* Use secondary color */
     flex-shrink: 0;
}

.step-content {
     flex-grow: 1;
}
.step-content h4 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.2rem;
    color: var(--color-secondary);
}
.step-content p {
    margin-bottom: 0.8rem;
    font-size: 1rem;
}
.step-details {
    background-color: var(--color-bg-light);
    border: 1px dashed var(--color-border);
    padding: 0.8rem;
    border-radius: 8px;
    font-size: 0.9rem;
    color: var(--color-text-light);
    margin-top: 1rem; /* Add space above details */
}
 .step-details p {
     margin-bottom: 0;
     font-size: 0.9rem;
 }

/* --- Packet Analysis --- */
.packet-analysis {
    display: grid;
    grid-template-columns: 1fr; /* Stack on small screens */
    gap: 2rem;
    margin-top: 2rem;
}

.packet {
    background-color: var(--color-bg-medium);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    border: 1px solid var(--color-border);
}

.packet h3 {
    margin-top: 0;
    margin-bottom: 1.5rem;
    font-size: 1.3rem;
    text-align: center;
}
.packet.tcp h3 { color: var(--color-tcp); }
.packet.udp h3 { color: var(--color-udp); }

.packet-diagram {
    display: flex;
    flex-wrap: wrap;
    /* gap: 2px; Minimal gap - Replaced by border approach */
    background-color: var(--color-bg-light);
    border: 1px solid var(--color-border);
    border-radius: 8px;
    overflow: hidden; /* Clip corners */
    margin-bottom: 1rem;
}

.packet-field {
    padding: 0.6rem 0.8rem;
    font-size: 0.75rem;
    text-align: center;
    border: 1px solid var(--color-border); /* Use border instead of gap */
    margin: -1px 0 0 -1px; /* Overlap borders */
    flex-grow: 1;
    background-color: #e8eaf6; /* Light Indigo for TCP fields */
    color: var(--color-tcp);
}
.packet-diagram.udp .packet-field {
    background-color: #fff3e0; /* Light Orange for UDP fields */
    color: var(--color-udp);
}

.packet-field small {
    display: block;
    font-size: 0.65rem;
    color: var(--color-text-light);
    margin-top: 0.2rem;
}

/* Specific field widths for TCP */
.packet-diagram:not(.udp) .packet-field.source-port,
.packet-diagram:not(.udp) .packet-field.dest-port,
.packet-diagram:not(.udp) .packet-field.window,
.packet-diagram:not(.udp) .packet-field.checksum,
.packet-diagram:not(.udp) .packet-field.urgent { flex-basis: calc(50% + 1px); width: calc(50% + 1px);} /* 2 bytes */

.packet-diagram:not(.udp) .packet-field.sequence,
.packet-diagram:not(.udp) .packet-field.ack { flex-basis: calc(100% + 1px); width: calc(100% + 1px);} /* 4 bytes */

.packet-diagram:not(.udp) .packet-field.header-len { flex-basis: calc(25% + 1px); width: calc(25% + 1px);} /* 4 bits (approx) */
.packet-diagram:not(.udp) .packet-field.reserved { flex-basis: calc(37.5% + 1px); width: calc(37.5% + 1px);} /* 6 bits (approx) */
.packet-diagram:not(.udp) .packet-field.flags { flex-basis: calc(37.5% + 1px); width: calc(37.5% + 1px);} /* 6 bits (approx) */

.packet-diagram:not(.udp) .packet-field.options { flex-basis: calc(100% + 1px); width: calc(100% + 1px); background-color: #f5f5f5; color: var(--color-text); } /* Variable */
.packet-diagram:not(.udp) .packet-field.data { display: none; } /* Data is not part of header */


/* Specific field widths for UDP */
.packet-diagram.udp .packet-field.source-port,
.packet-diagram.udp .packet-field.dest-port,
.packet-diagram.udp .packet-field.length,
.packet-diagram.udp .packet-field.checksum { flex-basis: calc(50% + 1px); width: calc(50% + 1px); } /* 2 bytes */
.packet-diagram.udp .packet-field.data { display: none; } /* Data is not part of header */
.packet-diagram.udp .packet-field.large { display: none; } /* Hide placeholder if present */


.packet p {
    font-size: 0.95rem;
    text-align: center;
    margin-bottom: 0;
}

/* --- Conclusion --- */
.key-takeaways {
    background-color: #e8f5e9; /* Light green */
    border-left: 5px solid var(--color-secondary);
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 var(--border-radius) var(--border-radius) 0;
}
.key-takeaways h4 {
    margin-top: 0;
    color: var(--color-secondary);
    font-size: 1.2rem;
}
.key-takeaways ul {
    list-style: none;
    padding-left: 0;
    margin-bottom: 0;
}
.key-takeaways li {
    margin-bottom: 0.5rem;
    padding-left: 1.5em;
    position: relative;
}
.key-takeaways li::before {
    content: '✓';
    position: absolute;
    left: 0;
    color: var(--color-secondary);
    font-weight: bold;
}

.motivational-quote blockquote {
    font-style: italic;
    background: #fff9c4; /* Light yellow */
    border-left: 5px solid #ffeb3b; /* Yellow */
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 var(--border-radius) var(--border-radius) 0;
    font-size: 1.1rem;
    color: #5d4037; /* Brownish text */
}
 .motivational-quote blockquote p { margin-bottom: 0; }


/* --- Resources --- */
.resources-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
}

.resource-card {
    display: block; /* Make the whole card clickable */
    background-color: var(--color-bg-light);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    text-align: center;
    box-shadow: var(--box-shadow);
    border: 1px solid var(--color-border);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    color: var(--color-text); /* Ensure text color is default */
}

.resource-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--box-shadow-hover);
    text-decoration: none; /* Remove underline on hover */
    color: var(--color-primary); /* Change text color on hover */
}

.resource-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: var(--color-primary);
}

.resource-card h4 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.1rem;
    color: inherit; /* Inherit color from parent link */
}
.resource-card p {
    font-size: 0.9rem;
    color: var(--color-text-light);
    margin-bottom: 0;
}

/* --- Social Share / Footer --- */
 .post-footer { /* Style the footer area */
     margin-top: 3rem;
     padding-top: 2rem;
     border-top: 1px solid var(--color-border);
     text-align: center;
 }
.social-share h3 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.3rem;
    color: var(--color-text);
}
.social-share p {
    margin-bottom: 1.5rem;
    font-size: 1rem;
}

.share-buttons {
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap; /* Allow wrapping on small screens */
}

.share-button {
    display: inline-block;
    padding: 0.8rem 1.5rem;
    border-radius: 25px; /* Pill shape */
    color: white !important; /* Ensure white text */
    font-weight: bold;
    text-transform: uppercase;
    font-size: 0.9rem;
    transition: background-color 0.3s ease, transform 0.2s ease;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    text-decoration: none !important; /* Remove underline */
}
.share-button:hover {
    text-decoration: none !important; /* Ensure no underline on hover */
    transform: scale(1.05);
}

.share-button.twitter { background-color: #1DA1F2; }
.share-button.linkedin { background-color: #0A66C2; }
.share-button.facebook { background-color: #1877F2; }

.share-button.twitter:hover { background-color: #0c85d0; }
.share-button.linkedin:hover { background-color: #0855a0; }
.share-button.facebook:hover { background-color: #125cb9; }

/* --- Responsive Adjustments --- */
@media (max-width: 768px) {
    .post-content-jekyll h1:not(.hero-post h1) { font-size: 2.2rem; }
    .hero-post h1 { font-size: 2.5rem; }
    .post-content-jekyll h2 { font-size: 1.8rem; }
    .post-content-jekyll h3 { font-size: 1.4rem; }

    .container {
        margin: 1rem auto;
        padding: 0 0.5rem;
    }

    .protocol-comparison {
        grid-template-columns: 1fr; /* Stack TCP/UDP cards */
        gap: 1.5rem;
    }

    .handshake-step {
        flex-direction: column;
        align-items: stretch; /* Stretch items */
        gap: 1rem;
    }
     .step-devices {
         min-width: unset; /* Remove min-width */
         justify-content: space-between; /* Space out devices/arrow */
         width: 100%;
     }
     .arrow {
         flex-grow: 1; /* Allow arrow to take space */
     }


    .multiplexing-container {
        grid-template-columns: 1fr;
    }
     .multiplex-illustration {
         flex-direction: column;
         gap: 1.5rem;
     }
     .multiplex-arrows {
         transform: rotate(90deg); /* Point arrows down */
     }

    .packet-analysis {
        grid-template-columns: 1fr;
    }

    .resources-grid {
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    }

    .share-buttons {
        flex-direction: column;
        align-items: center;
    }
    .share-button {
        width: 80%;
        max-width: 250px;
    }
}

@media (max-width: 480px) {
     .post-content-jekyll h1:not(.hero-post h1) { font-size: 1.8rem; }
    .hero-post h1 { font-size: 2rem; }
    .post-content-jekyll h2 { font-size: 1.5rem; }
    .post-content-jekyll h3 { font-size: 1.2rem; }
    .post-content-jekyll p { font-size: 1rem;}

    .functions-grid {
         grid-template-columns: 1fr; /* Single column */
    }

    .port-examples {
        justify-content: center; /* Center ports */
    }
    .port-example {
        min-width: 150px; /* Allow more wrapping */
    }

    /* Adjust packet field sizes for very small screens */
    .packet-field {
        font-size: 0.7rem;
        padding: 0.4rem 0.6rem;
    }
    .packet-field small {
        font-size: 0.6rem;
    }
}

/* Call to action */
.cta-container {
  background-color: #f5f9ff;
  border: 1px solid #e1e8ed;
  border-radius: 8px;
  padding: 1.5rem;
  margin-top: 2rem;
}

.cta-container h4 {
  color: #0693e3;
  margin-top: 0;
}

.cta-container ul {
  margin-bottom: 0;
}

.cta-container a {
  color: #0693e3;
  text-decoration: none;
}
</style>
