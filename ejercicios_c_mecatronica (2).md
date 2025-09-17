# Catálogo de Ejercicios - Introducción a la Programación en C
## Enfoque Mecatrónica - Universidad

### Estructura del Repositorio
```
ejercicios-c-mecatronica/
├── README.md
├── 01-algoritmos-basicos/
├── 02-operadores/
├── 03-variables/
├── 04-estructuras-decision/
├── 05-ciclos-repetitivos/
├── 06-arreglos/
├── 07-funciones/
├── proyectos-integradores/
└── recursos/
```

---

## 1. ALGORITMOS BÁSICOS (30 ejercicios)

### Nivel Básico (1-10)
1. **Cálculo de velocidad angular**: Dado el número de RPM de un motor, calcular la velocidad angular en rad/s
2. **Conversión de temperatura**: Convertir temperatura de Celsius a Kelvin para sensores
3. **Cálculo de potencia eléctrica**: P = V × I, dados voltaje y corriente
4. **Tiempo de caída libre**: Calcular tiempo que tarda un objeto en caer desde altura h
5. **Frecuencia a período**: Convertir frecuencia de una señal a su período
6. **Cálculo de torque**: T = F × d, dados fuerza y distancia
7. **Velocidad lineal**: v = ω × r, dada velocidad angular y radio
8. **Energía cinética**: Ec = ½mv², dados masa y velocidad
9. **Resistencia equivalente en serie**: Sumar resistencias en serie
10. **Cálculo de aceleración**: a = (vf - vi) / t

### Nivel Intermedio (11-20)
11. **Cálculo de eficiencia de motor**: η = (Potencia_salida / Potencia_entrada) × 100
12. **Conversión de unidades de presión**: Pa a bar, psi, etc.
13. **Cálculo de momento de inercia**: I = m × r² para disco
14. **Tensión en resorte**: F = k × x (Ley de Hooke)
15. **Cálculo de caudal**: Q = A × v, dados área y velocidad
16. **Conversión de coordenadas**: Cartesianas a polares
17. **Cálculo de capacitancia equivalente**: Capacitores en paralelo
18. **Velocidad crítica de eje rotatorio**: Cálculo básico
19. **Factor de seguridad**: FS = Resistencia_material / Esfuerzo_aplicado
20. **Cálculo de inductancia**: Para bobina simple

### Nivel Avanzado (21-30)
21. **Ecuación de Bernoulli simplificada**: Cálculo de presión en fluidos
22. **Cálculo de deflexión en viga**: Fórmula simplificada
23. **Respuesta de sistema de primer orden**: Constante de tiempo
24. **Cálculo de par de apriete**: Dados coeficiente de fricción y fuerza
25. **Conversión de sistemas de numeración**: Decimal a binario (algoritmo)
26. **Cálculo de ganancia de amplificador**: dB = 20 × log10(Vout/Vin)
27. **Análisis dimensional**: Verificar consistencia de ecuaciones
28. **Cálculo de centro de gravedad**: Para formas simples
29. **Transformada de Laplace básica**: Para funciones simples
30. **Cálculo de impedancia**: Z = √(R² + (ωL)²)

---

## 2. OPERADORES (30 ejercicios)

### Nivel Básico (1-10)
1. **Estados de bits en control**: Usar operadores bit a bit para encender/apagar LEDs
2. **Calculadora básica**: Implementar +, -, ×, ÷ con validación
3. **Comparador de sensores**: Comparar lecturas de dos sensores de temperatura
4. **Detector de paridad**: Verificar si un número es par o impar (bit menos significativo)
5. **Escalamiento de señales**: Escalar valor de sensor (0-1023) a voltaje (0-5V)
6. **Operaciones lógicas básicas**: AND, OR, NOT para control de actuadores
7. **Cálculo de módulo**: Usar % para crear señales periódicas
8. **Incremento/decremento**: Contador de pulsos de encoder
9. **División entera**: Calcular número de revoluciones completas
10. **Precedencia de operadores**: Evaluación de expresiones complejas

### Nivel Intermedio (11-20)
11. **Máscara de bits**: Extraer bits específicos de registro de estado
12. **Rotación de bits**: Simular registro de desplazamiento
13. **Operador ternario**: Seleccionar entre dos valores de referencia
14. **XOR para toggle**: Alternar estado de salidas
15. **Operaciones con punto flotante**: Precisión en cálculos de control
16. **Overflow detection**: Detectar desbordamiento en contadores
17. **Conversión implícita**: Mezclar int y float en cálculos
18. **Operadores de asignación combinada**: +=, -=, etc. para acumuladores
19. **Comparación de flotantes**: Implementar tolerancia en comparaciones
20. **Manipulación de registros**: Configurar registros de microcontrolador

### Nivel Avanzado (21-30)
21. **Campo de bits (bitfield)**: Empaquetado de estados de sistema
22. **Aritmética modular**: Para generación de formas de onda
23. **Operaciones saturadas**: Limitar valores entre máximo y mínimo
24. **Detección de flancos**: Rising/falling edge en señales digitales
25. **Multiplicación por potencias de 2**: Optimización con shift left
26. **División rápida**: Optimización con shift right
27. **Checksum calculation**: Verificación de integridad de datos
28. **Gray code conversion**: Convertir binario a código Gray
29. **BCD operations**: Operaciones en código BCD
30. **Fixed-point arithmetic**: Aritmética de punto fijo para DSP

---

## 3. VARIABLES (30 ejercicios)

### Nivel Básico (1-10)
1. **Declaración de constantes**: Definir constantes físicas (π, g, c)
2. **Variables de sensor**: Almacenar lecturas de temperatura, presión, humedad
3. **Estados de sistema**: Variables booleanas para estados de máquina
4. **Contadores**: Variables para contar eventos, pulsos, ciclos
5. **Temporizadores**: Variables para medir tiempo transcurrido
6. **Coordenadas**: Variables para posición x, y, z de robot
7. **Parámetros de motor**: RPM, torque, corriente, voltaje
8. **Configuración de sistema**: Variables para parámetros ajustables
9. **Buffer de datos**: Variables para almacenar datos temporalmente
10. **Flags de estado**: Variables para indicar estado de procesos

### Nivel Intermedio (11-20)
11. **Scope de variables**: Local vs global en sistemas de control
12. **Variables estáticas**: Mantener estado entre llamadas a función
13. **Punteros básicos**: Apuntar a variables de configuración
14. **Arrays de sensores**: Arreglo para múltiples sensores del mismo tipo
15. **Estructuras básicas**: Agrupar datos relacionados de un motor
16. **Enumeraciones**: Estados de una máquina de estados
17. **Union para datos**: Interpretar bytes como entero o float
18. **Variables volátiles**: Para registros de hardware
19. **Constantes simbólicas**: #define para pines y configuraciones
20. **Typedef**: Crear tipos personalizados para claridad

### Nivel Avanzado (21-30)
21. **Punteros a función**: Seleccionar algoritmo de control dinámicamente
22. **Arrays multidimensionales**: Matriz de transformación 3D
23. **Estructuras complejas**: Sistema complejo con múltiples subsistemas
24. **Listas enlazadas básicas**: Cola de comandos pendientes
25. **Memoria dinámica**: malloc/free para buffers variables
26. **Variables de registro**: Mapear variables a registros de hardware
27. **Bit fields avanzados**: Estructura para registro de control compacto
28. **Alineación de memoria**: Optimizar estructuras para eficiencia
29. **Variables thread-safe**: Compartir datos entre procesos
30. **Memory mapping**: Mapear dispositivos de hardware en memoria

---

## 4. ESTRUCTURAS DE DECISIÓN (30 ejercicios)

### Nivel Básico (1-10)
1. **Control de temperatura**: if-else para activar calefacción/refrigeración
2. **Límites de seguridad**: Verificar que presión esté en rango seguro
3. **Detector de movimiento**: Activar alarma si hay movimiento
4. **Selector de velocidad**: Elegir velocidad de motor según entrada
5. **Control de nivel**: if-else if para control de tanque de agua
6. **Clasificador de señales**: Clasificar señal como alta, media, baja
7. **Protección de sobrecarga**: Desconectar motor si corriente > límite
8. **Control de dirección**: Determinar dirección de giro de motor
9. **Validador de entrada**: Verificar que entrada esté en rango válido
10. **Selector de modo**: Elegir modo de operación (manual/automático)

### Nivel Intermedio (11-20)
11. **Estado de batería**: Switch-case para niveles de batería (crítico, bajo, normal, alto)
12. **Diagnóstico de fallas**: Múltiples condiciones para identificar tipo de falla
13. **Control de semáforo**: Lógica de estados de semáforo inteligente
14. **Selector de algoritmo**: Elegir algoritmo de control según condiciones
15. **Control de acceso**: Verificar múltiples condiciones de seguridad
16. **Planificador de tareas**: Decidir qué tarea ejecutar según prioridades
17. **Control de calidad**: Clasificar productos según múltiples parámetros
18. **Sistema de emergencia**: Jerarquía de respuestas a emergencias
19. **Control adaptativo**: Cambiar parámetros según condiciones ambientales
20. **Máquina de estados básica**: Estados de un proceso automatizado

### Nivel Avanzado (21-30)
21. **Control fuzzy básico**: Lógica difusa para control de temperatura
22. **Árbol de decisión**: Diagnóstico automatizado de fallas complejas
23. **Control predictivo**: Decisiones basadas en tendencias de datos
24. **Sistema experto básico**: Reglas de inferencia para mantenimiento
25. **Control por bandas**: Histéresis en control de sistemas
26. **Priorización dinámica**: Cambiar prioridades según estado del sistema
27. **Control tolerante a fallas**: Continuar operación con componentes dañados
28. **Optimización de ruta**: Elegir mejor camino según múltiples criterios
29. **Control adaptativo avanzado**: Autoajuste de parámetros PID
30. **Sistema de decisión multicriterio**: Evaluación ponderada de opciones

---

## 5. CICLOS REPETITIVOS (30 ejercicios)

### Nivel Básico (1-10)
1. **Muestreo de sensor**: Loop para leer sensor cada N milisegundos
2. **Contador de pulsos**: Contar pulsos de encoder hasta objetivo
3. **Generador de PWM**: Bucle para generar señal PWM por software
4. **Calibración de sensor**: Promedio de N lecturas para calibrar
5. **Búsqueda secuencial**: Buscar valor específico en array de datos
6. **Suma acumulativa**: Sumar serie de mediciones para promedio
7. **Temporizador por software**: Contador descendente hasta cero
8. **Parpadeo de LED**: Alternar estado de LED cada cierto tiempo
9. **Llenado de buffer**: Llenar array con valores iniciales
10. **Verificación periódica**: Revisar estado del sistema cada ciclo

### Nivel Intermedio (11-20)
11. **Control PID básico**: Loop de control con cálculos iterativos
12. **Filtro digital**: Implementar filtro pasa-bajas por software
13. **Búsqueda de máximo/mínimo**: Encontrar extremos en datos históricos
14. **Generación de tabla seno**: Precalcular tabla de valores trigonométricos
15. **Protocolo de comunicación**: Enviar/recibir datos en loop
16. **Máquina de estados cíclica**: Estados que se repiten periódicamente
17. **Algoritmo de ordenamiento**: Ordenar array de sensores por valor
18. **Control de motores paso a paso**: Secuencia de pasos repetitiva
19. **Monitoreo continuo**: Supervisar múltiples parámetros constantemente
20. **Algoritmo de búsqueda binaria**: Búsqueda eficiente en datos ordenados

### Nivel Avanzado (21-30)
21. **FFT básica**: Transformada rápida de Fourier iterativa
22. **Control de trayectoria**: Seguimiento de ruta con múltiples waypoints
23. **Algoritmo genético simple**: Optimización evolutiva básica
24. **Red neuronal básica**: Entrenamiento iterativo de perceptrón
25. **Control adaptativo**: Ajuste automático de parámetros en tiempo real
26. **Procesamiento de imagen**: Filtros y operaciones sobre matrices de píxeles
27. **Simulación de sistema dinámico**: Integración numérica paso a paso
28. **Algoritmo de clustering**: Agrupación k-means de datos de sensores
29. **Control predictivo por modelo**: Optimización de horizonte recesivo
30. **Algoritmo de pathfinding**: A* para navegación de robots

---

## 6. ARREGLOS (30 ejercicios)

### Nivel Básico (1-10)
1. **Array de sensores**: Almacenar lecturas de múltiples sensores de temperatura
2. **Historial de datos**: Buffer circular para datos históricos
3. **Tabla de configuración**: Array con parámetros de configuración
4. **Mapa de bits**: Representar estado de múltiples actuadores
5. **Buffer de comunicación**: Array para datos de entrada/salida serie
6. **Coordenadas de robot**: Arrays para posiciones X, Y, Z
7. **Valores de calibración**: Tabla de corrección para sensores
8. **Estados de máquina**: Array de estados válidos del sistema
9. **Secuencia de comandos**: Array con secuencia de operaciones
10. **Datos de encoder**: Almacenar posiciones históricas de encoder

### Nivel Intermedio (11-20)
11. **Filtro FIR**: Implementar filtro de respuesta finita al impulso
12. **Tabla de lookup**: Precalcular valores de funciones complejas
13. **Buffer de audio**: Procesar muestras de audio en tiempo real
14. **Matriz de transformación**: Transformaciones 3D para brazo robótico
15. **Red de sensores**: Gestionar datos de red de sensores distribuidos
16. **Planificador de tareas**: Queue de tareas pendientes
17. **Control de servos**: Array de posiciones para múltiples servomotores
18. **Procesamiento de señales**: Ventanas deslizantes para análisis
19. **Sistema de alarmas**: Buffer de eventos y alarmas del sistema
20. **Control de pantalla**: Buffer de píxeles para display gráfico

### Nivel Avanzado (21-30)
21. **Convolución digital**: Implementar convolución discreta
22. **Matriz de rigidez**: Análisis de elementos finitos básico
23. **Red neuronal**: Pesos y biases en arrays multidimensionales
24. **Procesamiento de imágenes**: Operaciones sobre matrices de píxeles
25. **Control MIMO**: Sistemas multi-entrada multi-salida
26. **Análisis espectral**: FFT y análisis de frecuencias
27. **Filtro Kalman**: Implementación con matrices de estado
28. **Control de manipulador**: Cinemática directa e inversa con arrays
29. **Procesamiento de nubes de puntos**: Datos LIDAR en arrays 3D
30. **Sistema de visión**: Detección de objetos en imágenes

---

## 7. FUNCIONES (30 ejercicios) - **ENFOQUE PRINCIPAL**

### Nivel Básico (1-10)
1. **Función de conversión de unidades**: Celsius a Fahrenheit, metros a pies, etc.
2. **Calculadora de potencia**: `float calcular_potencia(float voltaje, float corriente)`
3. **Validador de rango**: `bool en_rango(float valor, float min, float max)`
4. **Función de promedio**: Calcular promedio de array de mediciones
5. **Convertidor de RPM**: `float rpm_to_rad_s(float rpm)`
6. **Función de redondeo**: Redondear lecturas de sensor a N decimales
7. **Calculadora de distancia**: Distancia euclidiana entre dos puntos
8. **Función de retardo**: `void delay_ms(int milisegundos)`
9. **Conversor de coordenadas**: Cartesianas a polares y viceversa
10. **Función de interpolación lineal**: Entre dos puntos de calibración

### Nivel Intermedio (11-20)
11. **Controlador PID**: `float pid_controller(float setpoint, float feedback, float dt)`
12. **Filtro pasa-bajas**: `float low_pass_filter(float input, float alpha)`
13. **Generador de PWM**: `void generate_pwm(int duty_cycle, int frequency)`
14. **Función de calibración**: Calibrar sensor con offset y ganancia
15. **Detectar flancos**: `bool detect_rising_edge(bool current, bool previous)`
16. **Función de histéresis**: Control on/off con histéresis
17. **Calculadora de RMS**: Valor RMS de señal AC
18. **Función de mapeo**: Mapear valor de un rango a otro
19. **Generador de trayectoria**: Puntos de trayectoria suave entre A y B
20. **Función de checksum**: Verificar integridad de datos

### Nivel Avanzado (21-30)
21. **Control adaptativo**: `void adaptive_control(SystemState* state)`
22. **Transformada de Fourier**: `void fft(Complex* signal, int N)`
23. **Cinemática directa**: `Position forward_kinematics(JointAngles angles)`
24. **Cinemática inversa**: `JointAngles inverse_kinematics(Position target)`
25. **Filtro Kalman**: `void kalman_filter(KalmanState* state, float measurement)`
26. **Control de impedancia**: Para robots de contacto con entorno
27. **Planificador de trayectoria**: A* pathfinding para robots móviles
28. **Control robusto**: Control H∞ básico para sistemas inciertos
29. **Estimador de estado**: Observer de Luenberger
30. **Control por modos deslizantes**: Sliding mode control básico

---

## PROYECTOS INTEGRADORES

### Proyecto 1: Sistema de Control de Temperatura
- Integrar sensores, actuadores, control PID, interfaz usuario
- Usar todas las estructuras de programación aprendidas

### Proyecto 2: Robot Seguidor de Línea
- Sensores, motores, lógica de decisión, control de velocidad
- Implementar máquina de estados y control en tiempo real

### Proyecto 3: Sistema de Monitoreo Industrial
- Múltiples sensores, comunicación serie, logging de datos
- Alarmas, interfaces, procesamiento de señales

### Proyecto 4: Brazo Robótico Simple
- Control de servos, cinemática, planificación de trayectorias
- Interfaz de comandos, seguridad, calibración

---

## METODOLOGÍA DE EVALUACIÓN

### Criterios de Evaluación:
1. **Funcionamiento correcto** (40%)
2. **Calidad del código** (30%)
3. **Eficiencia algorítmica** (15%)
4. **Documentación y comentarios** (15%)

### Progresión Sugerida:
1. **Semana 1-2**: Algoritmos básicos y operadores
2. **Semana 3-4**: Variables y estructuras de decisión
3. **Semana 5-6**: Ciclos repetitivos
4. **Semana 7-8**: Arreglos básicos
5. **Semana 9-12**: Funciones (énfasis principal)
6. **Semana 13-16**: Proyectos integradores

### Recursos Adicionales:
- Plantillas de código base
- Ejemplos resueltos
- Casos de prueba automatizados
- Documentación de APIs simuladas
- Videos explicativos de conceptos clave

---

*Este catálogo está diseñado para desarrollar progresivamente el pensamiento lógico computacional en estudiantes de mecatrónica, con énfasis especial en el uso efectivo de funciones para crear código modular, reutilizable y mantenible.*