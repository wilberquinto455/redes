---
layout: post
title: "La Capa de Transporte: El Puente Digital Entre Aplicaciones"
description: "Una explicación clara y visual de cómo la capa de transporte gestiona la comunicación entre aplicaciones en el mundo de las redes."
date: 2025-04-21
categories: [Redes, TCP/IP]
tags: [TCP, UDP, puertos, multiplexación, CCNA]
author: "Tu Nombre"
image: /assets/images/transport-layer.jpg
---
div class="container"> <header class="post-header">
        </header>

    <div class="hero-post">
      <h1>🚢 La Capa de Transporte</h1>
      <p class="subtitle">El puente que conecta tus aplicaciones con el mundo digital</p>
    </div>

    <article class="post-content">

        <section class="post-section">
          <h2>📌 Introducción</h2>
          <p>Imagina que cada aplicación en tu computadora es una empresa diferente dentro de un enorme edificio (tu dispositivo). La capa de transporte actúa como el servicio postal interno que se asegura de que cada carta (paquete de datos) llegue al departamento correcto. Su trabajo es vital: sin ella, tus correos electrónicos, videos de YouTube y videojuegos en línea no sabrían cómo encontrar su camino.</p>

          <div class="analogy-box">
            <div class="analogy-icon">💡</div>
            <div class="analogy-content">
              <h3>Analogía: El Sistema Postal Digital</h3>
              <p>Si la Internet fuera una ciudad, la capa de transporte sería el sistema postal. Las cartas (datos) necesitan direcciones (IP) para llegar al edificio correcto, pero también necesitan un número de oficina (puerto) para llegar al destinatario exacto dentro del edificio.</p>
            </div>
          </div>
        </section>

        <section class="post-section">
          <h2>🔍 ¿Qué hace exactamente la capa de transporte?</h2>

          <p>La capa de transporte tiene varias responsabilidades clave que permiten que tus aplicaciones se comuniquen a través de la red:</p>

          <div class="functions-grid">
            <div class="function-card">
              <div class="function-icon">🔢</div>
              <h3>Identificación de Aplicaciones</h3>
              <p>Usa números de puerto para dirigir los datos a la aplicación correcta. Es como si cada aplicación tuviera su propio buzón numerado.</p>
            </div>

            <div class="function-card">
              <div class="function-icon">✂️</div>
              <h3>Segmentación</h3>
              <p>Divide los grandes mensajes en segmentos más pequeños, como cortar una carta larga en varias páginas para que sea más fácil de enviar.</p>
            </div>

            <div class="function-card">
              <div class="function-icon">🔄</div>
              <h3>Control de Flujo</h3>
              <p>Regula la velocidad de envío para que el receptor no se vea abrumado, como un cartero que verifica si tu buzón tiene espacio antes de entregar más correo.</p>
            </div>

            <div class="function-card">
              <div class="function-icon">🛡️</div>
              <h3>Control de Errores</h3>
              <p>Verifica si hay datos dañados y, en algunos casos, solicita retransmisiones, actuando como un inspector de calidad para tus mensajes.</p>
            </div>
          </div>
        </section>

        <section class="post-section" id="tcp-udp">
          <h2>⚔️ TCP vs UDP: Los Dos Guerreros de la Capa de Transporte</h2>

          <p>La capa de transporte utiliza principalmente dos protocolos, cada uno con su propio conjunto de habilidades, como dos tipos diferentes de servicios de entrega:</p>

          <div class="protocol-comparison">
            <div class="protocol-card tcp">
              <div class="protocol-header">
                <div class="protocol-icon">🛡️</div>
                <h3>TCP: El Guardián Confiable</h3>
              </div>
              <div class="protocol-content">
                <p>El <strong>Transmission Control Protocol</strong> es como un servicio de entrega certificado con firma de recepción. Es meticuloso, cuidadoso y se asegura de que todo llegue perfectamente.</p>

                <h4>Características:</h4>
                <ul class="feature-list">
                  <li>Orientado a conexión: Establece un canal dedicado antes de enviar</li>
                  <li>Entrega garantizada: Si algo se pierde, lo reenvía</li>
                  <li>Ordenado: Mantiene la secuencia correcta de todos los datos</li>
                  <li>Control de congestión: Ajusta la velocidad según las condiciones de la red</li>
                </ul>

                <h4>Ideal para:</h4>
                <div class="use-cases">
                  <span class="use-case">Navegación web</span>
                  <span class="use-case">Correo electrónico</span>
                  <span class="use-case">Transferencia de archivos</span>
                  <span class="use-case">Aplicaciones bancarias</span>
                </div>
              </div>
            </div>

            <div class="protocol-card udp">
              <div class="protocol-header">
                <div class="protocol-icon">⚡</div>
                <h3>UDP: El Velocista Ligero</h3>
              </div>
              <div class="protocol-content">
                <p>El <strong>User Datagram Protocol</strong> es como un servicio de mensajería que lanza los paquetes y sigue adelante sin esperar confirmación. Es rápido, eficiente y no le importa si algún mensaje se pierde en el camino.</p>

                <h4>Características:</h4>
                <ul class="feature-list">
                  <li>Sin conexión: Envía datos sin establecer canal previo</li>
                  <li>No garantiza entrega: No hay reenvíos automáticos</li>
                  <li>Sin orden garantizado: Los paquetes pueden llegar desordenados</li>
                  <li>Ligero y rápido: Mínima sobrecarga en las comunicaciones</li>
                </ul>

                <h4>Ideal para:</h4>
                <div class="use-cases">
                  <span class="use-case">Videollamadas</span>
                  <span class="use-case">Streaming de video</span>
                  <span class="use-case">Juegos en línea</span>
                  <span class="use-case">DNS (nombres de dominio)</span>
                </div>
              </div>
            </div>
          </div>

          <div class="analogy-box">
            <div class="analogy-icon">💡</div>
            <div class="analogy-content">
              <h3>Analogía: Transportes en la vida real</h3>
              <p><strong>TCP es como un camión blindado:</strong> Seguro, confiable, confirma la entrega, pero más lento y pesado.</p>
              <p><strong>UDP es como una motocicleta de mensajería:</strong> Rápida, ágil, eficiente, pero sin garantías si hay problemas en el camino.</p>
            </div>
          </div>
        </section>

        <section class="post-section" id="handshake">
          <h2>🤝 El Saludo de Tres Vías (Three-Way Handshake)</h2>

          <p>Antes de que TCP comience a enviar datos, establece una conexión mediante un proceso llamado "saludo de tres vías" (Three-Way Handshake). Es como cuando dos personas establecen una llamada telefónica:</p>

          <div class="handshake-container">
            <div class="handshake-step">
              <div class="step-number">1</div>
              <div class="step-devices">
                <div class="device client">Cliente<br>🖥️</div>
                <div class="arrow">
                  <div class="arrow-label">SYN</div>
                  <div class="arrow-line">→</div>
                </div>
                <div class="device server">Servidor<br>🖧</div>
              </div>
              <div class="step-description">
                <h4>Solicitud de conexión (SYN)</h4>
                <p>"Hola, ¿podemos hablar?" - El cliente envía un bit SYN (sincronización) para iniciar la conexión.</p>
              </div>
            </div>

            <div class="handshake-step">
              <div class="step-number">2</div>
              <div class="step-devices">
                <div class="device client">Cliente<br>🖥️</div>
                <div class="arrow reverse">
                  <div class="arrow-label">SYN+ACK</div>
                  <div class="arrow-line">←</div>
                </div>
                <div class="device server">Servidor<br>🖧</div>
              </div>
              <div class="step-description">
                <h4>Aceptación (SYN-ACK)</h4>
                <p>"Sí, te escucho" - El servidor responde con un SYN-ACK (sincronización-reconocimiento).</p>
              </div>
            </div>

            <div class="handshake-step">
              <div class="step-number">3</div>
              <div class="step-devices">
                <div class="device client">Cliente<br>🖥️</div>
                <div class="arrow">
                  <div class="arrow-label">ACK</div>
                  <div class="arrow-line">→</div>
                </div>
                <div class="device server">Servidor<br>🖧</div>
              </div>
              <div class="step-description">
                <h4>Confirmación (ACK)</h4>
                <p>"¡Perfecto! Comencemos a hablar" - El cliente envía un ACK para confirmar y la conexión queda establecida.</p>
              </div>
            </div>
          </div>

          <div class="code-example">
            <h4>🔍 Ejemplo de captura de Wireshark de un Three-Way Handshake</h4>
            <pre><code># Three-Way Handshake cuando tu navegador conecta a un sitio web:
1. [Cliente → Servidor] TCP SYN Seq=0 Win=64240 Len=0 MSS=1460 WS=256 SACK_PERM=1
2. [Servidor → Cliente] TCP SYN, ACK Seq=0 Ack=1 Win=65535 Len=0 MSS=1460 WS=256 SACK_PERM=1
3. [Cliente → Servidor] TCP ACK Seq=1 Ack=1 Win=64240 Len=0
# Ahora la conexión está establecida y lista para transmitir datos (e.g., HTTP GET)</code></pre>
          </div>
        </section>

        <section class="post-section" id="ports">
          <h2>🚪 Puertos: Las Puertas a las Aplicaciones</h2>

          <p>Los puertos son números que identifican a qué aplicación va dirigido un paquete de datos. Son como extensiones telefónicas en una empresa: la dirección IP te lleva al edificio correcto, pero necesitas el número de puerto para llegar a la oficina específica.</p>

          <div class="ports-container">
            <div class="ports-group">
              <h3>Puertos bien conocidos (0-1023)</h3>
              <div class="port-examples">
                <div class="port-example">
                  <span class="port-number">80</span>
                  <span class="port-name">HTTP</span>
                  <span class="port-icon">🌐</span>
                </div>
                <div class="port-example">
                  <span class="port-number">443</span>
                  <span class="port-name">HTTPS</span>
                  <span class="port-icon">🔒</span>
                </div>
                <div class="port-example">
                  <span class="port-number">21</span>
                  <span class="port-name">FTP</span>
                  <span class="port-icon">📁</span>
                </div>
                <div class="port-example">
                  <span class="port-number">22</span>
                  <span class="port-name">SSH</span>
                  <span class="port-icon">🔑</span>
                </div>
                <div class="port-example">
                  <span class="port-number">25</span>
                  <span class="port-name">SMTP</span>
                  <span class="port-icon">📧</span>
                </div>
                 <div class="port-example">
                  <span class="port-number">53</span>
                  <span class="port-name">DNS</span>
                  <span class="port-icon">🗺️</span>
                </div>
              </div>
            </div>

            <div class="ports-group">
              <h3>Puertos registrados (1024-49151)</h3>
              <p>Usados por aplicaciones comunes como bases de datos (ej. MySQL: 3306), juegos y servicios personalizados.</p>
            </div>

            <div class="ports-group">
              <h3>Puertos dinámicos/privados (49152-65535)</h3>
              <p>Asignados temporalmente por el sistema operativo del cliente para conexiones salientes (puertos efímeros).</p>
            </div>
          </div>

          <div class="analogy-box">
            <div class="analogy-icon">💡</div>
            <div class="analogy-content">
              <h3>Analogía: El Gran Hotel IP</h3>
              <p>Piensa en un dispositivo como un enorme hotel. La dirección IP es la dirección del hotel, mientras que los puertos son los números de habitación. Cuando llega un paquete, el botones (la capa de transporte) mira el número de habitación (puerto de destino) para saber exactamente dónde entregarlo.</p>
            </div>
          </div>

          <div class="interactive-tip">
            <h4>👨‍💻 Pruébalo tú mismo</h4>
            <p>Para ver qué conexiones y puertos están activos en tu computadora, puedes usar estos comandos en la terminal:</p>

            <div class="command-tabs">
              <div class="command-tab active" data-os="windows">Windows</div>
              <div class="command-tab" data-os="linux">Linux/Mac</div>
            </div>

            <div class="command-content active" data-os="windows">
              <pre><code>netstat -ano | findstr "ESTABLISHED"</code></pre>
               <p><small>(Muestra conexiones TCP establecidas y el ID del proceso asociado)</small></p>
               <pre><code>netstat -ano | findstr "LISTENING"</code></pre>
               <p><small>(Muestra puertos TCP y UDP en escucha)</small></p>
            </div>

            <div class="command-content" data-os="linux">
               <pre><code>ss -tulnp | grep LISTEN</code></pre>
               <p><small>(Muestra puertos TCP y UDP en escucha con el proceso asociado - `ss` es más moderno que `netstat`)</small></p>
               <pre><code>ss -tanp</code></pre>
               <p><small>(Muestra todas las conexiones TCP activas con el proceso asociado)</small></p>
            </div>
          </div>
        </section>

        <section class="post-section" id="multiplexing">
          <h2>🔀 Multiplexación y Demultiplexación</h2>

          <p>La multiplexación permite que múltiples aplicaciones en un host envíen datos a través de una única interfaz de red. La demultiplexación es el proceso inverso en el receptor, entregando los datos a la aplicación correcta.</p>

          <div class="multiplexing-container">
            <div class="multiplex-section">
              <h3>Multiplexación (Salida)</h3>
              <div class="multiplex-illustration outgoing">
                <div class="app-container">
                  <div class="app">🎮 Juego<br><small>Origen: Puerto 51234</small></div>
                  <div class="app">📧 Email<br><small>Origen: Puerto 51235</small></div>
                  <div class="app">🎵 Música<br><small>Origen: Puerto 51236</small></div>
                </div>
                <div class="multiplex-arrows">➡️</div>
                <div class="transport-layer">
                  Capa de<br>Transporte<br>
                  <div class="tag">Multiplexación</div>
                </div>
                <div class="multiplex-arrows">➡️</div>
                <div class="network">
                  Internet
                </div>
              </div>
              <p>La capa de transporte <strong>recoge</strong> datos de diferentes sockets (aplicaciones), <strong>añade</strong> cabeceras (con puertos de origen/destino) y los <strong>pasa</strong> a la capa de red.</p>
            </div>

            <div class="multiplex-section">
              <h3>Demultiplexación (Entrada)</h3>
              <div class="multiplex-illustration incoming">
                <div class="network">
                  Internet
                </div>
                <div class="multiplex-arrows">➡️</div>
                <div class="transport-layer">
                  Capa de<br>Transporte<br>
                  <div class="tag">Demultiplexación</div>
                </div>
                <div class="multiplex-arrows">➡️</div>
                <div class="app-container">
                  <div class="app">🎮 Juego<br><small>Destino: Puerto 28960</small></div>
                  <div class="app">📧 Email<br><small>Destino: Puerto 143</small></div>
                  <div class="app">🎵 Música<br><small>Destino: Puerto 8080</small></div>
                </div>
              </div>
              <p>La capa de transporte <strong>recibe</strong> segmentos/datagramas de la capa de red, <strong>examina</strong> los puertos de destino y <strong>entrega</strong> los datos al socket/aplicación correcta.</p>
            </div>
          </div>

          <div class="real-example">
            <h4>📱 Ejemplo real: Tu teléfono inteligente</h4>
            <p>Cuando usas tu teléfono, puedes estar recibiendo notificaciones de WhatsApp (usando un puerto), actualizando tu feed de Instagram (otro puerto) y reproduciendo música en Spotify (otro puerto), todo simultáneamente sobre la misma conexión Wi-Fi o de datos móviles. La capa de transporte gestiona este tráfico múltiple usando los números de puerto.</p>
          </div>
        </section>

        <section class="post-section" id="case-study">
          <h2>🔬 Caso de estudio: Navegando por la web (HTTPS)</h2>

          <p>Veamos qué sucede con la capa de transporte cuando visitas <code>https://www.ejemplo.com</code>:</p>

          <div class="case-study-steps">
            <div class="case-step">
              <div class="step-number">1</div>
              <div class="step-content">
                <h4>Resolución DNS (UDP)</h4>
                <p>Tu navegador necesita la IP de "www.ejemplo.com". Envía una consulta DNS desde un puerto dinámico local al puerto 53 (DNS) de tu servidor DNS usando UDP.</p>
                <div class="step-details">
                  <p>UDP es rápido para esta simple consulta/respuesta. Si se pierde, la aplicación (navegador/SO) reintenta.</p>
                </div>
              </div>
            </div>

            <div class="case-step">
              <div class="step-number">2</div>
              <div class="step-content">
                <h4>Conexión TCP (Handshake)</h4>
                <p>Con la IP obtenida, tu navegador inicia una conexión TCP desde un puerto dinámico local al puerto 443 (HTTPS) del servidor web.</p>
                <div class="step-details">
                  <p>Se realiza el Three-Way Handshake (SYN → SYN/ACK → ACK) para establecer una conexión confiable.</p>
                </div>
              </div>
            </div>

             <div class="case-step">
              <div class="step-number">3</div>
              <div class="step-content">
                <h4>Negociación TLS (sobre TCP)</h4>
                <p>Se establece una conexión segura TLS/SSL sobre la conexión TCP existente. Esto implica un intercambio de certificados y claves.</p>
                <div class="step-details">
                  <p>TCP garantiza que todos los mensajes de la negociación TLS lleguen correctamente.</p>
                </div>
              </div>
            </div>

            <div class="case-step">
              <div class="step-number">4</div>
              <div class="step-content">
                <h4>Solicitud y Respuesta HTTP (cifrada)</h4>
                <p>Tu navegador envía la solicitud HTTP (ej. <code>GET /</code>) cifrada a través de la conexión TLS/TCP. El servidor responde con la página web (HTML, etc.) también cifrada.</p>
                <div class="step-details">
                  <p>TCP divide los datos en segmentos, los numera, asegura su entrega ordenada y gestiona el control de flujo.</p>
                </div>
              </div>
            </div>

            <div class="case-step">
              <div class="step-number">5</div>
              <div class="step-content">
                <h4>Transferencia de Recursos Adicionales</h4>
                <p>Para cargar imágenes, CSS, JS, etc., el navegador puede abrir conexiones TCP/TLS adicionales (o reutilizar existentes con HTTP/2+) al mismo servidor u otros.</p>
                <div class="step-details">
                  <p>Cada recurso se solicita y transfiere de forma segura y confiable usando TCP.</p>
                </div>
              </div>
            </div>

            <div class="case-step">
              <div class="step-number">6</div>
              <div class="step-content">
                <h4>Cierre de Conexión TCP</h4>
                <p>Una vez completada la transferencia (o tras un tiempo de inactividad), las conexiones TCP se cierran mediante un intercambio de paquetes FIN y ACK.</p>
                <div class="step-details">
                  <p>Esto libera los recursos (puertos, memoria) en ambos extremos.</p>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section class="post-section" id="practical-example">
          <h2>🧪 Análisis práctico: Cabeceras TCP y UDP</h2>

          <p>¿Cómo se ven realmente un segmento TCP o un datagrama UDP? Veamos la estructura de sus cabeceras:</p>

          <div class="packet-analysis">
            <div class="packet tcp">
              <h3>Estructura Cabecera TCP (mín. 20 Bytes)</h3>
              <div class="packet-diagram">
                <div class="packet-field source-port">Puerto Origen<br><small>2 bytes</small></div>
                <div class="packet-field dest-port">Puerto Destino<br><small>2 bytes</small></div>
                <div class="packet-field sequence">Número de Secuencia<br><small>4 bytes</small></div>
                <div class="packet-field ack">Número de ACK<br><small>4 bytes</small></div>
                <div class="packet-field header-len">HLEN<br><small>4 bits</small></div>
                <div class="packet-field reserved">Reservado<br><small>6 bits</small></div>
                <div class="packet-field flags">Flags (URG, ACK, PSH, RST, SYN, FIN)<br><small>6 bits</small></div>
                <div class="packet-field window">Tamaño Ventana<br><small>2 bytes</small></div>
                <div class="packet-field checksum">Checksum<br><small>2 bytes</small></div>
                <div class="packet-field urgent">Puntero Urgente<br><small>2 bytes</small></div>
                <div class="packet-field options">Opciones<br><small>Variable</small></div>
                </div>
              <p>La cabecera TCP contiene campos esenciales para la fiabilidad, el orden, el control de flujo y la gestión de la conexión.</p>
            </div>

            <div class="packet udp">
              <h3>Estructura Cabecera UDP (8 Bytes)</h3>
              <div class="packet-diagram udp">
                <div class="packet-field source-port">Puerto Origen<br><small>2 bytes</small></div>
                <div class="packet-field dest-port">Puerto Destino<br><small>2 bytes</small></div>
                <div class="packet-field length">Longitud (Cabecera+Datos)<br><small>2 bytes</small></div>
                <div class="packet-field checksum">Checksum (Opcional IPv4)<br><small>2 bytes</small></div>
                 </div>
              <p>La cabecera UDP es mínima, enfocada solo en la multiplexación/demultiplexación mediante puertos y la longitud del datagrama.</p>
            </div>
          </div>

          <div class="code-example">
            <h4>🔍 Ejemplo de análisis de Wireshark (Cabecera TCP)</h4>
            <pre><code>Transmission Control Protocol, Src Port: 54321, Dst Port: 443, Seq: 1, Ack: 1, Len: 517
    Source Port: 54321
    Destination Port: 443  // Conectando a HTTPS
    [Stream index: 1]
    [TCP Segment Len: 517]
    Sequence number: 1    (relative sequence number)
    Sequence number (raw): 123456789
    [Next sequence number: 518    (relative sequence number)]
    Acknowledgment number: 1    (relative ack number)
    Acknowledgment number (raw): 987654321
    Header Length: 32 bytes // Incluye opciones TCP
    Flags: 0x018 (PSH, ACK) // Push y Acknowledgment flags activos
        000. .... .... = Reserved: Not set
        ...0 .... .... = Nonce: Not set
        .... 0... .... = Congestion Window Reduced: Not set
        .... .0.. .... = ECN-Echo: Not set
        .... ..0. .... = Urgent: Not set
        .... ...1 .... = Acknowledgment: Set
        .... .... 1... = Push: Set
        .... .... .0.. = Reset: Not set
        .... .... ..0. = Syn: Not set
        .... .... ...0 = Fin: Not set
    Window size value: 64240
    [Calculated window size: 64240]
    Checksum: 0xabcd [validation disabled]
    Urgent pointer: 0
    Options: (12 bytes), No-Operation (NOP), No-Operation (NOP), Timestamps
        TCP Option - No-Operation (NOP)
        TCP Option - No-Operation (NOP)
        TCP Option - Timestamps: TSval 11111111, TSecr 22222222
[Timestamps]</code></pre>
          </div>
        </section>

        <section class="post-section" id="conclusion">
          <h2>📝 Conclusión</h2>

          <p>La capa de transporte es el motor silencioso pero fundamental que gestiona la comunicación entre las aplicaciones que usamos a diario en la red. Ya sea garantizando la entrega fiable de un correo electrónico con TCP o priorizando la velocidad para una videollamada con UDP, esta capa actúa como el puente indispensable entre el software y la infraestructura de red global.</p>

          <div class="key-takeaways">
            <h4>Puntos clave para recordar:</h4>
            <ul>
              <li>Es responsable de la comunicación lógica proceso a proceso (aplicación a aplicación).</li>
              <li>Proporciona multiplexación y demultiplexación usando números de puerto.</li>
              <li>Ofrece dos protocolos principales: TCP (fiable, orientado a conexión) y UDP (rápido, sin conexión).</li>
              <li>TCP utiliza mecanismos como números de secuencia, ACKs y control de flujo/congestión.</li>
              <li>UDP es ideal para aplicaciones sensibles a la latencia que pueden tolerar alguna pérdida.</li>
              <li>Comprenderla es crucial para el diagnóstico de problemas de red y el desarrollo de aplicaciones.</li>
            </ul>
          </div>

          <div class="motivational-quote">
            <blockquote>
              <p>"Dominar la capa de transporte te da la capacidad de entender no solo *si* los datos llegan, sino *cómo* y *por qué* llegan (o no) a su destino final en la aplicación."</p>
            </blockquote>
          </div>
        </section>

        <section class="post-section" id="resources">
          <h2>📚 Recursos adicionales</h2>

          <div class="resources-grid">
            <a href="#" class="resource-card" target="_blank" rel="noopener noreferrer"> <div class="resource-icon">📖</div>
              <h4>RFC 793 (TCP)</h4>
              <p>La especificación oficial de TCP.</p>
            </a>

            <a href="#" class="resource-card" target="_blank" rel="noopener noreferrer">
              <div class="resource-icon">📄</div>
              <h4>RFC 768 (UDP)</h4>
              <p>La especificación oficial de UDP.</p>
            </a>

            <a href="#" class="resource-card" target="_blank" rel="noopener noreferrer">
              <div class="resource-icon">🎬</div>
              <h4>Video: TCP Handshake Explained</h4>
              <p>Visualización del saludo de tres vías.</p>
            </a>

            <a href="#" class="resource-card" target="_blank" rel="noopener noreferrer">
              <div class="resource-icon">💻</div>
              <h4>Wireshark</h4>
              <p>Herramienta esencial para analizar tráfico.</p>
            </a>
          </div>
        </section>

    </article>

    <footer class="post-footer">
        <div class="social-share">
          <h3>¿Te resultó útil este artículo?</h3>
          <p>Compártelo en tus redes o deja un comentario.</p>
          <div class="share-buttons">
            <a href="#" class="share-button twitter" target="_blank" rel="noopener noreferrer">Compartir en Twitter</a>
            <a href="#" class="share-button linkedin" target="_blank" rel="noopener noreferrer">Compartir en LinkedIn</a>
            <a href="#" class="share-button facebook" target="_blank" rel="noopener noreferrer">Compartir en Facebook</a>
          </div>
        </div>
        </footer>

</div> <script>
    // Simple script for command tabs
    document.addEventListener('DOMContentLoaded', () => {
        const tabs = document.querySelectorAll('.command-tab');
        const contents = document.querySelectorAll('.command-content');

        tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                const os = tab.getAttribute('data-os');

                // Deactivate all tabs and content
                tabs.forEach(t => t.classList.remove('active'));
                contents.forEach(c => c.classList.remove('active'));

                // Activate clicked tab and corresponding content
                tab.classList.add('active');
                document.querySelector(`.command-content[data-os="${os}"]`).classList.add('active');
            });
        });
    });
</script>

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

        body {
            font-family: 'Inter', sans-serif; /* Use Inter font */
            line-height: 1.7; /* Improved readability */
            color: var(--color-text);
            background-color: var(--color-bg-light);
            margin: 0;
            padding: 0;
        }

        .container { /* Add a container for better centering and max-width */
            max-width: 900px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        /* --- Typography --- */
        h1, h2, h3, h4 {
            font-weight: 700;
            color: var(--color-text); /* Use dark text for headings */
            margin-top: 2.5rem;
            margin-bottom: 1.5rem;
        }

        h1 {
            font-size: 2.8rem;
            color: var(--color-primary);
            text-align: center;
        }

        h2 {
            font-size: 2rem;
            border-bottom: 2px solid var(--color-primary);
            padding-bottom: 0.5rem;
            color: var(--color-primary);
        }

        h3 {
            font-size: 1.5rem;
            color: var(--color-secondary);
        }

        h4 {
            font-size: 1.2rem;
            color: var(--color-text);
        }

        p {
            margin-bottom: 1.2rem;
            color: var(--color-text-light);
            font-size: 1.05rem; /* Slightly larger paragraph text */
        }

        a {
            color: var(--color-link);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: darken(var(--color-link), 10%);
            text-decoration: underline;
        }

        pre {
            background-color: var(--color-bg-dark);
            color: #f0f0f0;
            padding: 1.5rem;
            border-radius: var(--border-radius);
            overflow-x: auto;
            font-family: 'Courier New', Courier, monospace;
            font-size: 0.95rem;
            line-height: 1.5;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.2);
        }

        code {
             /* Inline code styling */
            background-color: #e0e0e0;
            padding: 0.2em 0.4em;
            border-radius: 4px;
            font-size: 0.9em;
            color: var(--color-text);
        }

        pre code { /* Reset inline code styles within pre blocks */
            background-color: transparent;
            padding: 0;
            border-radius: 0;
            font-size: inherit;
            color: inherit;
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

        .hero-post h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
            color: white;
            border-bottom: none; /* Remove border from H1 in hero */
        }

        .hero-post .subtitle {
            font-size: 1.4rem;
            opacity: 0.9;
            font-weight: 400;
            margin-top: 0;
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
        }

        .protocol-card.tcp .protocol-icon { background-color: var(--color-tcp); }
        .protocol-card.udp .protocol-icon { background-color: var(--color-udp); }

        .protocol-card h3 {
            margin: 0;
            font-size: 1.4rem;
        }
        .protocol-card.tcp h3 { color: var(--color-tcp); }
        .protocol-card.udp h3 { color: var(--color-udp); }

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
            gap: 2px; /* Minimal gap */
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
        .packet-field.source-port, .packet-field.dest-port,
        .packet-field.window, .packet-field.checksum, .packet-field.urgent { flex-basis: calc(50% - 1px); } /* 2 bytes */
        .packet-field.sequence, .packet-field.ack { flex-basis: calc(100% - 1px); } /* 4 bytes */
        .packet-field.header-len { flex-basis: calc(25% - 1px); } /* 4 bits (approx) */
        .packet-field.reserved, .packet-field.flags { flex-basis: calc(37.5% - 1px); } /* 6 bits (approx) */
        .packet-field.options, .packet-field.data { flex-basis: calc(100% - 1px); background-color: #f5f5f5; color: var(--color-text); } /* Variable */

        /* Specific field widths for UDP */
        .packet-diagram.udp .packet-field.source-port, .packet-diagram.udp .packet-field.dest-port,
        .packet-diagram.udp .packet-field.length, .packet-diagram.udp .packet-field.checksum { flex-basis: calc(50% - 1px); } /* 2 bytes */
        .packet-diagram.udp .packet-field.data { flex-basis: calc(100% - 1px); background-color: #f5f5f5; color: var(--color-text); } /* Variable */

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

        /* --- Social Share --- */
        .social-share {
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
        }

        .share-button {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            border-radius: 25px; /* Pill shape */
            color: white;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 0.9rem;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .share-button:hover {
            text-decoration: none;
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
            h1 { font-size: 2.2rem; }
            .hero-post h1 { font-size: 2.5rem; }
            h2 { font-size: 1.8rem; }
            h3 { font-size: 1.4rem; }

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
                align-items: flex-start; /* Align items left */
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
             h1 { font-size: 1.8rem; }
            .hero-post h1 { font-size: 2rem; }
            h2 { font-size: 1.5rem; }
            h3 { font-size: 1.2rem; }
            p { font-size: 1rem;}

            .functions-grid {
                 grid-template-columns: 1fr; /* Single column */
            }

            .port-examples {
                justify-content: center; /* Center ports */
            }
            .port-example {
                min-width: 150px; /* Allow more wrapping */
            }
        }

    </style>