---
layout: post # O el layout que uses para tus posts
title: "La Capa de Acceso a Red TCP/IP: Conectando al Medio Físico"
description: "Explorando la Capa de Acceso a Red del modelo TCP/IP, responsable de la transmisión física y el direccionamiento local (MAC)."
date: 2025-04-27 11:00:00 -0500 # Fecha sugerida, ajústala
categories: [redes]
tags: [TCP/IP, redes, CCNA, protocolos, capa de acceso a red, capa de enlace, capa fisica, Ethernet, Wi-Fi, MAC]
author: "Tu Nombre" # Reemplaza con tu nombre
image: /redes/assets/images/network-access-layer.jpg # Sugerencia de imagen, crea o busca una adecuada
# css: /assets/css/tcpip-layers.css # Asegúrate que este CSS esté enlazado en tu layout
---

<div class="container post-content-jekyll">

    <div class="hero-post">
        <h1>🔌 Capa de Acceso a Red TCP/IP</h1>
        <p class="subtitle">La conexión directa con cables, fibra y ondas de radio</p>
    </div>

    <article class="post-content">

        <section class="post-section">
            <h2>¿Qué es la Capa de Acceso a Red?</h2>

             <div class="analogy-box">
              <div class="analogy-icon"><i class="fas fa-ethernet"></i></div>
              <div class="analogy-content">
                <h3>La Función Principal</h3>
                <p>Esta capa, también conocida como Capa de Enlace, se encarga de todos los detalles necesarios para transmitir los paquetes IP sobre un <strong>medio físico específico</strong> (como un cable Ethernet, una conexión Wi-Fi, fibra óptica, etc.).</p>
                <p>Define cómo los dispositivos acceden al medio compartido, utiliza el <strong>direccionamiento físico (direcciones MAC)</strong> para la entrega local y prepara los datos para la transmisión física real. Esencialmente, combina las funciones de las capas de Enlace de Datos y Física del modelo OSI.</p>
              </div>
            </div>

            <p>Es la capa más baja del modelo TCP/IP y actúa como el puente final entre los datos lógicos (paquetes IP) y las señales físicas que viajan por los medios de red. Recibe los paquetes IP de la capa superior (Internet) y los adapta para la red local específica.</p>

             <h3>Componentes y Tecnologías Clave</h3>
             <div class="functions-grid">
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-network-wired"></i></div>
                <h4>Protocolos de Enlace</h4>
                <p>Definen el formato de las <strong>tramas</strong> (frames) y las reglas para la comunicación en un tipo de red específico (Ethernet, Wi-Fi 802.11, PPP, Frame Relay).</p>
              </div>
              <div class="function-card">
                <div class="function-icon"><i class="fas fa-address-card"></i></div>
                <h4>Direccionamiento Físico (MAC)</h4>
                <p>Utiliza direcciones MAC (Media Access Control), únicas para cada tarjeta de red, para identificar dispositivos dentro de la <strong>misma red local</strong>.</p>
              </div>
               <div class="function-card">
                <div class="function-icon"><i class="fas fa-broadcast-tower"></i></div>
                <h4>Control de Acceso al Medio (MAC)</h4>
                <p>Métodos para controlar cómo y cuándo un dispositivo puede transmitir en un medio compartido para evitar colisiones (CSMA/CD en Ethernet antiguo, CSMA/CA en Wi-Fi).</p>
              </div>
               <div class="function-card">
                <div class="function-icon"><i class="fas fa-plug"></i></div>
                <h4>Transmisión Física</h4>
                <p>Define las características eléctricas, ópticas o de radio para la señalización y codificación de bits sobre el medio físico (voltajes, frecuencias, modulación).</p>
              </div>
            </div>

             <h3>Ejemplo práctico</h3>

            <div class="example-details-box">
              <div class="example-header">
                <i class="fas fa-truck"></i>
                <h4>Ejemplo: Creación de Tramas Ethernet</h4>
              </div>
              <div class="example-content">
                <p>Retomando los paquetes IP que tu computadora quiere enviar (destinados a un servidor externo, pero que primero deben ir a tu router local):</p>
                <ol class="example-steps">
                  <li>La capa de Acceso a Red recibe cada paquete IP de la capa de Internet.</li>
                  <li>Determina el siguiente salto dentro de la red local. Usualmente es la dirección IP de tu router (gateway).</li>
                  <li>Utiliza el protocolo <strong>ARP (Address Resolution Protocol)</strong> para averiguar la dirección MAC de la tarjeta de red del router correspondiente a esa dirección IP del gateway. ARP básicamente pregunta en la red local: "¿Quién tiene la IP [IP del router]? Dime tu MAC".</li>
                  <li>Una vez obtenida la MAC del router, encapsula el paquete IP dentro de una <strong>trama Ethernet</strong> (si estás conectado por cable). Esta trama incluye:
                      <ul>
                          <li><strong>Dirección MAC de Destino:</strong> La dirección MAC de la interfaz de red de tu router.</li>
                          <li><strong>Dirección MAC de Origen:</strong> La dirección MAC de tu propia tarjeta de red.</li>
                          <li>Un campo de Tipo/EtherType (ej. 0x0800 para indicar que los datos son un paquete IPv4).</li>
                          <li>Una Secuencia de Verificación de Trama (FCS) al final para detectar errores de transmisión.</li>
                      </ul>
                  </li>
                  <li>Finalmente, la parte física de esta capa convierte los bits (0s y 1s) de la trama en señales eléctricas que se envían por el cable Ethernet hacia el switch o router.</li>
                </ol>
                 <div class="analogy-box">
                  <div class="analogy-icon">🚚</div>
                  <div class="analogy-content">
                    <h3>Analogía: El Camión de Reparto Local</h3>
                    <p><strong>La Capa de Acceso a Red es como la empresa de logística y transporte dentro de tu ciudad:</strong></p>
                    <ul>
                      <li>Recibe los sobres con dirección completa del cartero principal (paquetes IP).</li>
                      <li>Sabe que para salir de la ciudad, primero debe llevar el sobre al centro de distribución principal (router/gateway).</li>
                      <li>Pregunta en la oficina: "¿Cuál es el número exacto del muelle de carga del centro de distribución?" (ARP para obtener la MAC del router).</li>
                      <li>Mete el sobre en una caja estándar para transporte local (trama Ethernet).</li>
                      <li>En la etiqueta de la caja escribe:
                          <ul>
                            <li>Número del muelle de destino dentro de la ciudad (MAC destino: router).</li>
                            <li>Tu número de muelle de origen (MAC origen: tu PC).</li>
                          </ul>
                      </li>
                      <li>Le da la caja al conductor del camión (tarjeta de red física).</li>
                      <li>El conductor (componente físico) arranca el camión y conduce por las calles específicas de la ciudad (cable Ethernet, ondas Wi-Fi) siguiendo las normas de tráfico locales (CSMA/CD o CSMA/CA) hasta llegar al muelle correcto del centro de distribución.</li>
                    </ul>
                  </div>
                </div>
                 <div class="code-example">
                     <h4>Trama Ethernet II (Simplificada)</h4>
                     <pre><code>MAC Destino: 00:1A:2B:3C:4D:5E (MAC del Router)
MAC Origen: 00:AA:BB:CC:DD:EE (Tu MAC)
EtherType: 0x0800 (IPv4)
--- Datos (Paquete IP Completo) ---
FCS: (Checksum de la trama calculado por hardware)
</code></pre>
                </div>
              </div>
            </div>

             <p>Esta capa es fundamental porque adapta la comunicación lógica de IP a las particularidades de cada tecnología de red física, permitiendo que diferentes tipos de redes (Ethernet, Wi-Fi, etc.) puedan interconectarse y transportar paquetes IP.</p>

        </section>

    </article>

    <footer class="post-footer">
        </footer>

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
