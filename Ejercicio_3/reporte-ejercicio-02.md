### 1. Gemini 

- **Performance:** Maximizar la satisfacción del usuario, minimizar el gasto computacional, maximizar la utilidad de las respuestas.
- **Environment:** Parcialmente observable, estocástico, secuencial, dinámico. Internet, entorno virtual del usuario.
- **Actuators:** Generar texto, crear imágenes, responder preguntas, usar herramientas (buscar en web, ejecutar código).
- **Sensors:** Interfaz de chat (teclado/prompt), cámara, micrófono, herramientas conectadas, historial de conversación.

### 2. Roomba

- **Performance:** Porcentaje de limpieza, velocidad para terminar, minimizar el gasto eléctrico, no chocar o quedarse atorada.
- **Environment:** Dinámico, estocástico, parcialmente observable, secuencial, continuo. Adentro o afuera de una casa, pisos, muebles, personas, mascotas.
- **Actuators:** Activar aspiradora, avanzar, retroceder, girar, encender cepillos laterales, emitir sonidos de alerta.
- **Sensors:** Cámara, sensor de choque (bumper), sensor de suciedad, sensor de caída (para escaleras), sensor de calor.

### 3. Spotify recomendador

- **Performance:** Minutos de música escuchada, tiempo en la aplicación, número de canciones recomendadas a las que el usuario dio "like".
- **Environment:** Dinámico, estocástico, parcialmente observable, secuencial, discreto. Catálogo de canciones, álbumes, usuarios.
- **Actuators:** Añadir canción al feed del usuario, generar playlist personalizada, enviar notificaciones.
- **Sensors:** Métricas de usuario (clicks, tiempo de reproducción, skips, likes/dislikes), historial de búsqueda, base de datos de usuarios similares.

### 4. Tesla (Autopilot)

- **Performance:** Velocidad para llegar de un destino a otro, seguridad (no chocar), comodidad del viaje, respetar leyes de tránsito.
- **Environment:** Parcialmente observable, estocástico, dinámico, continuo. Calles, peatones, topes, tráfico, clima.
- **Actuators:** Acelerar, frenar, girar el volante, encender luces, poner direccionales, tocar el claxon.
- **Sensors:** Cámaras (delanteras y traseras), radar, GPS, micrófono, sensores ultrasónicos, velocímetro, mapa.

### 5. Agente de Trading

- **Performance:** Ganancias por minuto (ROI), ganancia total, minimizar riesgos y pérdidas.
- **Environment:** Mercados financieros, bolsas de valores. Parcialmente observable, estocástico, dinámico, secuencial. Dinero y acciones.
- **Actuators:** Comprar acciones, vender acciones, mantener (hold) posición.
- **Sensors:** Internet, APIs de precios en tiempo real, feeds de noticias financieras, historial de precios.

### 6. Diagnóstico Médico

- **Performance:** Cantidad de diagnósticos correctos, velocidad del diagnóstico, precisión, evitar falsos positivos/negativos.
- **Environment:** Hospital, consultorio. Parcialmente observable, estocástico, episódico (cada paciente es un caso independiente). Pacientes y expedientes.
- **Actuators:** Emitir diagnóstico, imprimir receta, sugerir tratamientos, ordenar más estudios.
- **Sensors:** Teclado (para meter síntomas al sistema), cámara, resultados de laboratorio, bases de datos médicas.

### 7. Dron de inspección

- **Performance:** Precisión al detectar fallas en estructuras, área cubierta, tiempo de vuelo sin agotar batería, evitar accidentes.
- **Environment:** Lugares abiertos, infraestructura (puentes, antenas). Parcialmente observable, dinámico, continuo, estocástico (clima, viento).
- **Actuators:** Acelerar hélices, controlar altitud, girar, ajustar ángulo de la cámara, tomar foto o grabar video.
- **Sensors:** GPS, cámara de alta resolución, giroscopio, sensor de proximidad (LiDAR), altímetro, indicador de batería.

### 8. Ajedrez Engine

- **Performance:** Ganar la partida, capturar piezas importantes, dar jaque mate rápido, no perder por tiempo.
- **Environment:** Tablero de ajedrez. Totalmente observable, determinista, secuencial, estático, discreto, multiagente (el rival).
- **Actuators:** Mover pieza en el tablero (o mostrar la jugada en la pantalla).
- **Sensors:** Entrada del usuario (teclado/ratón para ver la jugada del rival), reloj de tiempo.
