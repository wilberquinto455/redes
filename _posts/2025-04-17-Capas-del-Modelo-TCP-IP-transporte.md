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

<!-- Hero del artículo -->
<div class="hero-post">
  <h1>🚢 La Capa de Transporte</h1>
  <p class="subtitle">El puente que conecta tus aplicaciones con el mundo digital</p>
</div>

<!-- Introducción -->
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

<!-- ¿Qué hace la capa de transporte? -->
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

<!-- TCP vs UDP -->
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
          <li>✅ <strong>Orientado a conexión</strong>: Establece un canal dedicado antes de enviar</li>
          <li>✅ <strong>Entrega garantizada</strong>: Si algo se pierde, lo reenvía</li>
          <li>✅ <strong>Ordenado</strong>: Mantiene la secuencia correcta de todos los datos</li>
          <li>✅ <strong>Control de congestión</strong>: Ajusta la velocidad según las condiciones de la red</li>
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
          <li>✅ <strong>Sin conexión</strong>: Envía datos sin establecer canal previo</li>
          <li>✅ <strong>No garantiza entrega</strong>: No hay reenvíos automáticos</li>
          <li>✅ <strong>Sin orden garantizado</strong>: Los paquetes pueden llegar desordenados</li>
          <li>✅ <strong>Ligero y rápido</strong>: Mínima sobrecarga en las comunicaciones</li>
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

<!-- Ejemplo visual del Three-Way Handshake -->
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
    <pre><code>
# Three-Way Handshake cuando tu navegador conecta a un sitio web:
1. [Cliente → Servidor] TCP SYN Seq=0 Win=64240
2. [Servidor → Cliente] TCP SYN+ACK Seq=0 Ack=1 Win=65535
3. [Cliente → Servidor] TCP ACK Seq=1 Ack=1 Win=64240
# Ahora la conexión está establecida y lista para transmitir datos
    </code></pre>
  </div>
</section>

<!-- Puertos -->
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
      </div>
    </div>
    
    <div class="ports-group">
      <h3>Puertos registrados (1024-49151)</h3>
      <p>Usados por aplicaciones comunes como bases de datos, juegos y servicios personalizados.</p>
    </div>
    
    <div class="ports-group">
      <h3>Puertos dinámicos (49152-65535)</h3>
      <p>Asignados temporalmente para conexiones salientes y comunicaciones efímeras.</p>
    </div>
  </div>

  <div class="analogy-box">
    <div class="analogy-icon">💡</div>
    <div class="analogy-content">
      <h3>Analogía: El Gran Hotel IP</h3>
      <p>Piensa en un dispositivo como un enorme hotel. La dirección IP es la dirección del hotel, mientras que los puertos son los números de habitación. Cuando llega un paquete, el botones (la capa de transporte) mira el número de habitación (puerto) para saber exactamente dónde entregarlo.</p>
    </div>
  </div>

  <div class="interactive-tip">
    <h4>👨‍💻 Pruébalo tú mismo</h4>
    <p>Para ver qué conexiones y puertos están activos en tu computadora, puedes usar estos comandos:</p>
    
    <div class="command-tabs">
      <div class="command-tab" data-os="windows">Windows</div>
      <div class="command-tab" data-os="linux">Linux/Mac</div>
      
      <div class="command-content" data-os="windows">
        <pre><code>netstat -an | findstr "ESTABLISHED"</code></pre>
      </div>
      
      <div class="command-content" data-os="linux">
        <pre><code>netstat -tuln | grep LISTEN</code></pre>
      </div>
    </div>
  </div>
</section>

<!-- Multiplexación y demultiplexación -->
<section class="post-section" id="multiplexing">
  <h2>🔀 Multiplexación: El Arte de Combinar Múltiples Conversaciones</h2>
  
  <p>La multiplexación es como cuando varias personas comparten una misma línea telefónica. Permite que múltiples aplicaciones usen la misma conexión de red simultáneamente:</p>
  
  <div class="multiplexing-container">
    <div class="multiplex-section">
      <h3>Multiplexación</h3>
      <div class="multiplex-illustration outgoing">
        <div class="app-container">
          <div class="app">🎮 Juego<br><small>Puerto 28960</small></div>
          <div class="app">📧 Email<br><small>Puerto 143</small></div>
          <div class="app">🎵 Música<br><small>Puerto 8080</small></div>
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
      <p>La capa de transporte <strong>combina</strong> datos de diferentes aplicaciones, añadiendo información de puerto para identificar su origen.</p>
    </div>
    
    <div class="multiplex-section">
      <h3>Demultiplexación</h3>
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
          <div class="app">🎮 Juego<br><small>Puerto 28960</small></div>
          <div class="app">📧 Email<br><small>Puerto 143</small></div>
          <div class="app">🎵 Música<br><small>Puerto 8080</small></div>
        </div>
      </div>
      <p>La capa de transporte <strong>separa</strong> los datos recibidos y los entrega a la aplicación correcta según el número de puerto de destino.</p>
    </div>
  </div>

  <div class="real-example">
    <h4>📱 Ejemplo real: Tu teléfono inteligente</h4>
    <p>Cuando usas tu teléfono, puedes estar recibiendo notificaciones de WhatsApp, actualizando tu feed de Instagram y reproduciendo música en Spotify, todo al mismo tiempo. La capa de transporte se encarga de que cada bit de información llegue a la aplicación correcta.</p>
  </div>
</section>

<!-- Caso de estudio -->
<section class="post-section" id="case-study">
  <h2>🔬 Caso de estudio: Navegando por la web</h2>
  
  <p>Veamos qué sucede con la capa de transporte cuando visitas una página web:</p>
  
  <div class="case-study-steps">
    <div class="case-step">
      <div class="step-number">1</div>
      <div class="step-content">
        <h4>Resolución DNS (usando UDP)</h4>
        <p>Tu navegador necesita traducir "www.ejemplo.com" a una dirección IP. Envía una consulta UDP al puerto 53 (DNS) de tu servidor DNS.</p>
        <div class="step-details">
          <p>UDP es perfecto aquí porque es una consulta rápida y simple. Si se pierde, simplemente se reintenta.</p>
        </div>
      </div>
    </div>
    
    <div class="case-step">
      <div class="step-number">2</div>
      <div class="step-content">
        <h4>Establecimiento de conexión TCP</h4>
        <p>Una vez que tu navegador conoce la IP del sitio web, establece una conexión TCP con el servidor web en el puerto 443 (HTTPS).</p>
        <div class="step-details">
          <p>Aquí es donde ocurre el Three-Way Handshake explicado anteriormente.</p>
        </div>
      </div>
    </div>
    
    <div class="case-step">
      <div class="step-number">3</div>
      <div class="step-content">
        <h4>Solicitud y respuesta HTTP</h4>
        <p>Tu navegador envía una solicitud HTTP a través de la conexión TCP. El servidor procesa la solicitud y devuelve la página web.</p>
        <div class="step-details">
          <p>TCP garantiza que todos los paquetes que componen la página web lleguen correctamente y en orden.</p>
        </div>
      </div>
    </div>
    
    <div class="case-step">
      <div class="step-number">4</div>
      <div class="step-content">
        <h4>Transferencia de recursos</h4>
        <p>Para cargar imágenes, CSS, JavaScript y otros recursos, el navegador puede establecer conexiones TCP adicionales al mismo servidor.</p>
        <div class="step-details">
          <p>Los navegadores modernos establecen múltiples conexiones TCP para cargar los recursos en paralelo y acelerar la carga de la página.</p>
        </div>
      </div>
    </div>
    
    <div class="case-step">
      <div class="step-number">5</div>
      <div class="step-content">
        <h4>Cierre de conexión</h4>
        <p>Una vez completada la transferencia, se cierran las conexiones TCP mediante un proceso de cuatro pasos (FIN-ACK).</p>
        <div class="step-details">
          <p>Este proceso libera los recursos del servidor y del cliente para otras conexiones.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Ejemplo práctico avanzado -->
<section class="post-section" id="practical-example">
  <h2>🧪 Análisis práctico: Diseccionando un paquete</h2>
  
  <p>¿Cómo se ve realmente un segmento TCP o un datagrama UDP? Veamos la estructura de ambos:</p>
  
  <div class="packet-analysis">
    <div class="packet tcp">
      <h3>Estructura de un segmento TCP</h3>
      <div class="packet-diagram">
        <div class="packet-field source-port">Puerto Origen<br><small>2 bytes</small></div>
        <div class="packet-field dest-port">Puerto Destino<br><small>2 bytes</small></div>
        <div class="packet-field sequence">Número de Secuencia<br><small>4 bytes</small></div>
        <div class="packet-field ack">Número de ACK<br><small>4 bytes</small></div>
        <div class="packet-field header-len">HLEN<br><small>4 bits</small></div>
        <div class="packet-field reserved">Reservado<br><small>6 bits</small></div>
        <div class="packet-field flags">Flags<br><small>6 bits</small></div>
        <div class="packet-field window">Ventana<br><small>2 bytes</small></div>
        <div class="packet-field checksum">Checksum<br><small>2 bytes</small></div>
        <div class="packet-field urgent">Puntero Urgente<br><small>2 bytes</small></div>
        <div class="packet-field options">Opciones<br><small>Variable</small></div>
        <div class="packet-field data">Datos<br><small>Variable</small></div>
      </div>
      <p>Un segmento TCP tiene una cabecera de 20 bytes (sin opciones) con campos para control de secuencia, control de flujo, y detección de errores.</p>
    </div>
    
    <div class="packet udp">
      <h3>Estructura de un datagrama UDP</h3>
      <div class="packet-diagram udp">
        <div class="packet-field source-port">Puerto Origen<br><small>2 bytes</small></div>
        <div class="packet-field dest-port">Puerto Destino<br><small>2 bytes</small></div>
        <div class="packet-field length">Longitud<br><small>2 bytes</small></div>
        <div class="packet-field checksum">Checksum<br><small>2 bytes</small></div>
        <div class="packet-field data large">Datos<br><small>Variable</small></div>
      </div>
      <p>Un datagrama UDP tiene una cabecera de solo 8 bytes, lo que lo hace más ligero y rápido, pero con menos capacidades de control.</p>
    </div>
  </div>

  <div class="code-example">
    <h4>🔍 Ejemplo de análisis de Wireshark</h4>
    <pre><code>
# Captura de una solicitud HTTP utilizando TCP
Frame 42: 74 bytes on wire
Ethernet II, Src: Dell_12:34:56 (00:14:22:12:34:56), Dst: Cisco_78:9a:bc (00:1a:2b:78:9a:bc)
Internet Protocol Version 4, Src: 192.168.1.10, Dst: 93.184.216.34
Transmission Control Protocol, Src Port: 54321, Dst Port: 80, Seq: 1, Ack: 1
    Source Port: 54321
    Destination Port: 80
    Sequence number: 1    (relative sequence number)
    Acknowledgment number: 1    (relative ack number)
    Header Length: 20 bytes
    Flags: 0x018 (PSH, ACK)
    Window size value: 64240
    Checksum: 0x5a32 [validation disabled]
Hypertext Transfer Protocol
    GET / HTTP/1.1\r\n
    Host: example.com\r\n
    Connection: keep-alive\r\n
    ...
    </code></pre>
  </div>
</section>

<!-- Conclusión -->
<section class="post-section" id="conclusion">
  <h2>📝 Conclusión</h2>
  
  <p>La capa de transporte es el componente esencial que hace posible que múltiples aplicaciones utilicen la red simultáneamente. Es el puente que conecta tus aplicaciones con el vasto mundo de Internet, asegurando que cada bit de información llegue a su destino correcto.</p>
  
  <div class="key-takeaways">
    <h4>Puntos clave para recordar:</h4>
    <ul>
      <li>✅ La capa de transporte es responsable de la comunicación extremo a extremo entre aplicaciones</li>
      <li>✅ TCP proporciona conexiones confiables pero con mayor sobrecarga</li>
      <li>✅ UDP ofrece velocidad pero sin garantías de entrega</li>
      <li>✅ Los puertos permiten identificar a qué aplicación pertenecen los datos</li>
      <li>✅ La multiplexación permite que múltiples aplicaciones compartan la conexión de red</li>
    </ul>
  </div>
  
  <div class="motivational-quote">
    <blockquote>
      "Comprender la capa de transporte es como tener las llaves del reino digital: sabrás exactamente cómo fluyen los datos de una aplicación a otra."
    </blockquote>
  </div>
</section>

<!-- Recursos adicionales -->
<section class="post-section" id="resources">
  <h2>📚 Recursos adicionales</h2>
  
  <div class="resources-grid">
    <a href="#" class="resource-card">
      <div class="resource-icon">📖</div>
      <h4>Guía completa de TCP/IP</h4>
      <p>Profundiza en todos los aspectos del modelo TCP/IP</p>
    </a>
    
    <a href="#" class="resource-card">
      <div class="resource-icon">🎬</div>
      <h4>Video tutorial: TCP vs UDP</h4>
      <p>Visualiza las diferencias con ejemplos animados</p>
    </a>
    
    <a href="#" class="resource-card">
      <div class="resource-icon">💻</div>
      <h4>Laboratorio práctico</h4>
      <p>Captura y analiza tu propio tráfico de red</p>
    </a>
    
    <a href="#" class="resource-card">
      <div class="resource-icon">🧩</div>
      <h4>Quiz interactivo</h4>
      <p>Pon a prueba tus conocimientos sobre la capa de transporte</p>
    </a>
  </div>
</section>

<!-- Compartir y comentarios -->
<div class="social-share">
  <h3>¿Te resultó útil este artículo?</h3>
  <p>Compártelo con tus colegas o deja un comentario abajo.</p>
  <div class="share-buttons">
    <a href="#" class="share-button twitter">Twitter</a>
    <a href="#" class="share-button linkedin">LinkedIn</a>
    <a href="#" class="share-button facebook">Facebook</a>
  </div>
</div>

<style>
/* Estilos generales */
:root {
  --color-primary: #0277bd;
  --color-secondary: #00c853;
  --color-tcp: #3949ab;
  --color-udp: #e65100;
  --color-bg-light: #f5f7fa;
  --color-bg-dark: #263238;
  --color-text: #37474f;
  --color-text-light: #78909c;
  --color-border: #cfd8dc;
  --color-link: #039be5;
  --border-radius: 8px;
  --box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

body {
  font-family: 'Roboto', 'Segoe UI', Arial, sans-serif;
  line-height: 1.6;
  color: var(--color-text);
}

.post-section {
  margin-bottom: 3rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--color-border);
}

h2 {
  color: var(--color-primary);
  margin-top: 2rem;
  margin-bottom: 1.5rem;
  font-weight: 700;
  font-size: 1.8rem;
}

h3 {
  color: var(--color-primary);
  margin-top: 1.5rem;
  margin-bottom: 1rem;
  font-size: 1.4rem;
}


<style>
/* Estilos para el artículo del modelo OSI */
.post-content {
  font-family: 'Roboto', sans-serif;
  line-height: 1.6;
  color: #333;
}

.post-content h2 {
  margin-top: 2rem;
  margin-bottom: 1rem;
  color: #0693e3;
  border-bottom: 2px solid #eaeaea;
  padding-bottom: 0.5rem;
}

.post-content h3 {
  margin-top: 1.5rem;
  color: #0693e3;
}

/* Caja de información */
.info-box {
  background-color: #e8f4fd;
  border-left: 5px solid #0693e3;
  padding: 1rem;
  margin: 1.5rem 0;
  border-radius: 0 5px 5px 0;
  display: flex;
  align-items: flex-start;
}

.info-icon {
  font-size: 1.5rem;
  color: #0693e3;
  margin-right: 1rem;
}

/* Contenedor del modelo OSI */
.osi-model-container {
  display: flex;
  flex-direction: column;
  gap: 5px;
  margin: 2rem 0;
}

.osi-layer {
  display: flex;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.layer-number {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 3rem;
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
  background-color: rgba(0,0,0,0.2);
}

.layer-content {
  padding: 1rem;
  flex-grow: 1;
  color: #333;
}

.layer-content h3 {
  margin: 0 0 0.5rem 0;
  color: #333;
}

.layer-content p {
  margin: 0 0 0.5rem 0;
}

.layer-examples {
  font-size: 0.9rem;
  font-style: italic;
}

/* Beneficios grid */
.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.benefit-card {
  background-color: #f5f9ff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  transition: transform 0.3s ease;
}

.benefit-card:hover {
  transform: translateY(-5px);
}

.benefit-icon {
  font-size: 1.8rem;
  color: #0693e3;
  margin-bottom: 1rem;
}

.benefit-card h4 {
  color: #0693e3;
  margin: 0 0 0.5rem 0;
}

.benefit-card p {
  margin: 0;
  font-size: 0.95rem;
}

/* Diagrama de encapsulamiento */
.encapsulation-diagram {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin: 2rem 0;
  max-width: 600px;
}

.encap-step {
  display: flex;
  align-items: center;
  background-color: #f5f9ff;
  padding: 1rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.encap-icon {
  font-size: 1.5rem;
  color: #0693e3;
  margin-right: 1rem;
  min-width: 2rem;
  text-align: center;
}

.encap-content {
  flex-grow: 1;
}

.encap-content h4 {
  margin: 0 0 0.25rem 0;
  color: #0693e3;
}

.encap-content p {
  margin: 0;
  font-size: 0.9rem;
}

.encap-arrow {
  text-align: center;
  color: #0693e3;
  font-size: 1.2rem;
}

/* Tabla de comparación */
.comparison-table {
  margin: 2rem 0;
  overflow-x: auto;
}

.comparison-table table {
  width: 100%;
  border-collapse: collapse;
}

.comparison-table th, .comparison-table td {
  border: 1px solid #ddd;
  padding: 0.75rem;
  text-align: center;
}

.comparison-table th {
  background-color: #0693e3;
  color: white;
}

.comparison-table tr:nth-child(even) {
  background-color: #f2f2f2;
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

.cta-container a:hover {
  text-decoration: underline;
}

/* Responsive */
@media (max-width: 768px) {
  .benefits-grid {
    grid-template-columns: 1fr;
  }
  
  .osi-layer {
    flex-direction: column;
  }
  
  .layer-number {
    width: 100%;
    padding: 0.5rem 0;
  }
}

.protocols-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); /* Ajusta el ancho mínimo según sea necesario */
  gap: 20px;
  margin-top: 20px;
}

.protocol-card {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  display: flex; /* Añadido para centrar el contenido verticalmente */
  flex-direction: column;
  align-items: center; /* Centra los elementos horizontalmente */
  text-align: center; /* Centra el texto dentro de la tarjeta */
}

.protocol-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
}

.protocol-card i {
  font-size: 40px; /* Aumenta el tamaño del icono */
  margin-bottom: 15px;
  color: #007bff; /* Un color que resalte, como el azul de Bootstrap */
}

.protocol-card h4 {
  margin-bottom: 10px;
  color: #333; /* Color de texto más oscuro para el encabezado */
}

.protocol-card p {
  font-size: 1rem;
  color: #555; /* Color de texto un poco más suave */
  line-height: 1.5; /* Mejora la legibilidad del texto */
}

.example-box {
  background-color: #e6f7fc;
  padding: 20px;
  margin: 20px 0;
  border-radius: 10px;
  border: 1px solid #ced4da;
}

.example-header {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.example-header i {
  font-size: 24px;
  margin-right: 10px;
  color: #28a745; /* Un color llamativo para el icono del ejemplo */
}

.example-header h4 {
  margin: 0;
  color: #2c3e50; /* Color de texto más oscuro para el título del ejemplo */
}

.example-content p {
  margin-bottom: 10px;
  font-size: 1rem;
  color: #555;
}

.example-steps {
  list-style-position: inside;
  padding-left: 0;
  margin-bottom: 15px;
  font-size: 1rem;
  color: #555;
}

.example-steps li {
  margin-bottom: 5px;
}

.code-snippet {
  color: #ffffff;
  background-color: #000000;
  padding: 15px;
  border-radius: 5px;
  margin-bottom: 15px;
  overflow-x: auto;
  font-family: monospace;
  font-size: 0.9rem;
  border: 1px solid #ddd;
}

.code-snippet pre {
  margin: 0;
  white-space: pre-wrap;
}

/* Estilos adicionales para mejorar la apariencia general */
.post-content {
  font-family: 'Arial', sans-serif; /* Cambia la fuente para una mejor lectura */
  line-height: 1.7; /* Aumenta el interlineado para más espacio entre líneas */
}


.post-content h3 {
  margin-top: 25px;
  color: #3498db; /* Azul más vivo para los subtítulos */
  font-size: 1.5rem; /* Aumenta el tamaño del subtítulo */
}

.post-content p {
  font-size: 1.1rem; /* Aumenta el tamaño de la fuente del párrafo */
  color: #555;
}

/* Ajustes para pantallas más pequeñas */
@media (max-width: 768px) {
  .protocols-grid {
    grid-template-columns: 1fr; /* Volver a una sola columna en pantallas pequeñas */
  }
  
  .protocol-card {
    padding: 15px; /* Reduce el padding en pantallas pequeñas */
  }
  
  .protocol-card i {
    font-size: 32px; /* Reduce el tamaño del icono en pantallas pequeñas */
  }
  
  .example-header i {
    font-size: 20px; /* Reduce el tamaño del icono del ejemplo en pantallas pequeñas */
  }
}

.hero-post {
  background: var(--color-bg-acento);
  color: white;
  padding: 2rem;
  border-radius: 2xl;
  margin-bottom: 1.5rem;
}

.subtitle {
  font-size: 1.25rem;
  opacity: 0.9;
}

.post-section {
  margin-bottom: 2rem;
}

.info-box {
  background-color: #f0f4ff;
  border-left: 4px solid #4f8cf5;
  padding: 1rem;
  margin: 1rem 0;
  border-radius: 0.5rem;
}

.checklist li {
  list-style: none;
  padding-left: 1.5em;
  text-indent: -1.2em;
}

.checklist li::before {
  content: "✔️ ";
  padding-right: 0.5em;
}

.card-box {
  background-color: #eafbee;
  padding: 1rem;
  border-radius: 1rem;
  margin-top: 1rem;
}

.motivational-quote blockquote {
  font-style: italic;
  background: #fff9e6;
  border-left: 4px solid #ffc107;
  padding: 1rem;
  margin: 2rem 0;
  border-radius: 0.5rem;
}

.social-share {
  margin-top: 2rem;
  text-align: center;
}

</style>