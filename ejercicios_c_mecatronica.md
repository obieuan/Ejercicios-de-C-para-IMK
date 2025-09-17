# Ejercicios de Programación en C - Mecatrónica
## Semana de Práctica Intensiva

### Instrucciones Generales
- Cada ejercicio tiene un **prototipo de función** que debes implementar
- El `main()` ya incluye **test cases** para validar tu implementación
- **NO modifiques** los prototipos de función ni los test cases
- **Compila y ejecuta** cada programa para verificar que pase todas las pruebas
- Los ejercicios integran: **variables, operadores, estructuras de decisión, ciclos, arreglos y funciones**

---

## EJERCICIO 1: Control de Velocidad de Motor
**Contexto**: Convertir RPM a velocidad angular para control de motor DC

```c
// Prototipo de función
float rpm_to_rad_per_sec(int rpm);

// Test case en main()
int main() {
    printf("Test 1: rpm_to_rad_per_sec(1500) = %.2f (esperado: 157.08)\n", rpm_to_rad_per_sec(1500));
    printf("Test 2: rpm_to_rad_per_sec(0) = %.2f (esperado: 0.00)\n", rpm_to_rad_per_sec(0));
    printf("Test 3: rpm_to_rad_per_sec(3000) = %.2f (esperado: 314.16)\n", rpm_to_rad_per_sec(3000));
    return 0;
}
```

---

## EJERCICIO 2: Sensor de Temperatura Industrial
**Contexto**: Convertir lecturas de sensor de °C a Kelvin

```c
// Prototipo de función
float celsius_to_kelvin(float celsius);

// Test case en main()
int main() {
    printf("Test 1: celsius_to_kelvin(25.5) = %.2f (esperado: 298.65)\n", celsius_to_kelvin(25.5));
    printf("Test 2: celsius_to_kelvin(0.0) = %.2f (esperado: 273.15)\n", celsius_to_kelvin(0.0));
    printf("Test 3: celsius_to_kelvin(-40.0) = %.2f (esperado: 233.15)\n", celsius_to_kelvin(-40.0));
    return 0;
}
```

---

## EJERCICIO 3: Monitor de Potencia Eléctrica
**Contexto**: Calcular potencia consumida por actuadores

```c
// Prototipo de función
float calculate_power(float voltage, float current);

// Test case en main()
int main() {
    printf("Test 1: calculate_power(220.0, 5.2) = %.2f (esperado: 1144.00)\n", calculate_power(220.0, 5.2));
    printf("Test 2: calculate_power(12.0, 0.5) = %.2f (esperado: 6.00)\n", calculate_power(12.0, 0.5));
    printf("Test 3: calculate_power(0.0, 10.0) = %.2f (esperado: 0.00)\n", calculate_power(0.0, 10.0));
    return 0;
}
```

---

## EJERCICIO 4: Validador de Rango de Sensor
**Contexto**: Verificar que lectura de sensor esté en rango válido

```c
// Prototipo de función
int is_in_range(float value, float min_val, float max_val);

// Test case en main()
int main() {
    printf("Test 1: is_in_range(25.5, 0.0, 100.0) = %d (esperado: 1)\n", is_in_range(25.5, 0.0, 100.0));
    printf("Test 2: is_in_range(-5.0, 0.0, 100.0) = %d (esperado: 0)\n", is_in_range(-5.0, 0.0, 100.0));
    printf("Test 3: is_in_range(50.0, 25.0, 75.0) = %d (esperado: 1)\n", is_in_range(50.0, 25.0, 75.0));
    return 0;
}
```

---

## EJERCICIO 5: Control de Sistema de Calefacción
**Contexto**: Determinar acción de control basada en temperatura

```c
// Prototipo de función (0=apagar, 1=calentar, 2=enfriar)
int heating_control(float current_temp, float setpoint, float tolerance);

// Test case en main()
int main() {
    printf("Test 1: heating_control(18.0, 22.0, 1.0) = %d (esperado: 1)\n", heating_control(18.0, 22.0, 1.0));
    printf("Test 2: heating_control(25.0, 22.0, 1.0) = %d (esperado: 2)\n", heating_control(25.0, 22.0, 1.0));
    printf("Test 3: heating_control(22.5, 22.0, 1.0) = %d (esperado: 0)\n", heating_control(22.5, 22.0, 1.0));
    return 0;
}
```

---

## EJERCICIO 6: Contador de Pulsos de Encoder
**Contexto**: Contar pulsos válidos en array de señales digitales

```c
// Prototipo de función
int count_pulses(int signals[], int size);

// Test case en main()
int main() {
    int test1[] = {0, 1, 0, 1, 0, 1, 0};
    int test2[] = {1, 1, 1, 1, 1};
    int test3[] = {0, 0, 0, 0};
    
    printf("Test 1: count_pulses(test1, 7) = %d (esperado: 3)\n", count_pulses(test1, 7));
    printf("Test 2: count_pulses(test2, 5) = %d (esperado: 5)\n", count_pulses(test2, 5));
    printf("Test 3: count_pulses(test3, 4) = %d (esperado: 0)\n", count_pulses(test3, 4));
    return 0;
}
```

---

## EJERCICIO 7: Promedio de Lecturas de Sensor
**Contexto**: Calcular promedio de múltiples lecturas para filtrar ruido

```c
// Prototipo de función
float sensor_average(float readings[], int count);

// Test case en main()
int main() {
    float test1[] = {23.5, 24.1, 23.8, 24.2, 23.9};
    float test2[] = {100.0};
    float test3[] = {10.5, 15.3, 8.7, 12.1};
    
    printf("Test 1: sensor_average(test1, 5) = %.2f (esperado: 23.90)\n", sensor_average(test1, 5));
    printf("Test 2: sensor_average(test2, 1) = %.2f (esperado: 100.00)\n", sensor_average(test2, 1));
    printf("Test 3: sensor_average(test3, 4) = %.2f (esperado: 11.65)\n", sensor_average(test3, 4));
    return 0;
}
```

---

## EJERCICIO 8: Generador de PWM por Software
**Contexto**: Generar array de señal PWM con duty cycle específico

```c
// Prototipo de función (llena array con 0s y 1s según duty_cycle)
void generate_pwm(int output[], int size, int duty_cycle);

// Test case en main()
int main() {
    int pwm1[10], pwm2[10], pwm3[4];
    
    generate_pwm(pwm1, 10, 50);  // 50% duty cycle
    generate_pwm(pwm2, 10, 25);  // 25% duty cycle  
    generate_pwm(pwm3, 4, 75);   // 75% duty cycle
    
    printf("Test 1 (50%% duty): ");
    for(int i = 0; i < 10; i++) printf("%d ", pwm1[i]);
    printf("\n");
    
    printf("Test 2 (25%% duty): ");
    for(int i = 0; i < 10; i++) printf("%d ", pwm2[i]);
    printf("\n");
    
    printf("Test 3 (75%% duty): ");
    for(int i = 0; i < 4; i++) printf("%d ", pwm3[i]);
    printf("\n");
    
    return 0;
}
```

---

## EJERCICIO 9: Detector de Sobrecarga en Motor
**Contexto**: Detectar si corriente del motor excede límite por tiempo determinado

```c
// Prototipo de función
int detect_overload(float currents[], int size, float limit, int min_violations);

// Test case en main()
int main() {
    float test1[] = {2.1, 2.3, 3.8, 4.1, 3.9, 2.0};  // límite 3.5A
    float test2[] = {1.0, 1.2, 1.1, 1.3};
    float test3[] = {4.0, 4.1, 3.0, 4.2, 4.3};
    
    printf("Test 1: detect_overload(test1, 6, 3.5, 2) = %d (esperado: 1)\n", detect_overload(test1, 6, 3.5, 2));
    printf("Test 2: detect_overload(test2, 4, 3.5, 2) = %d (esperado: 0)\n", detect_overload(test2, 4, 3.5, 2));
    printf("Test 3: detect_overload(test3, 5, 3.5, 3) = %d (esperado: 1)\n", detect_overload(test3, 5, 3.5, 3));
    return 0;
}
```

---

## EJERCICIO 10: Conversión de Coordenadas para Robot
**Contexto**: Convertir coordenadas cartesianas a polares para navegación

```c
// Prototipo de función (calcula distancia desde origen)
float cartesian_to_distance(float x, float y);

// Test case en main()
int main() {
    printf("Test 1: cartesian_to_distance(3.0, 4.0) = %.2f (esperado: 5.00)\n", cartesian_to_distance(3.0, 4.0));
    printf("Test 2: cartesian_to_distance(0.0, 5.0) = %.2f (esperado: 5.00)\n", cartesian_to_distance(0.0, 5.0));
    printf("Test 3: cartesian_to_distance(-3.0, -4.0) = %.2f (esperado: 5.00)\n", cartesian_to_distance(-3.0, -4.0));
    return 0;
}
```

---

## EJERCICIO 11: Control de Velocidad Variable
**Contexto**: Mapear valor de potenciómetro (0-1023) a PWM (0-255)

```c
// Prototipo de función
int map_value(int input, int in_min, int in_max, int out_min, int out_max);

// Test case en main()
int main() {
    printf("Test 1: map_value(512, 0, 1023, 0, 255) = %d (esperado: 127)\n", map_value(512, 0, 1023, 0, 255));
    printf("Test 2: map_value(1023, 0, 1023, 0, 255) = %d (esperado: 255)\n", map_value(1023, 0, 1023, 0, 255));
    printf("Test 3: map_value(0, 0, 1023, 50, 200) = %d (esperado: 50)\n", map_value(0, 0, 1023, 50, 200));
    return 0;
}
```

---

## EJERCICIO 12: Filtro Digital Pasa-Bajas
**Contexto**: Implementar filtro simple para suavizar señales de sensores

```c
// Prototipo de función (filtro: output = alpha * input + (1-alpha) * prev_output)
float low_pass_filter(float input, float previous_output, float alpha);

// Test case en main()
int main() {
    printf("Test 1: low_pass_filter(10.0, 5.0, 0.3) = %.2f (esperado: 6.50)\n", low_pass_filter(10.0, 5.0, 0.3));
    printf("Test 2: low_pass_filter(0.0, 10.0, 0.1) = %.2f (esperado: 9.00)\n", low_pass_filter(0.0, 10.0, 0.1));
    printf("Test 3: low_pass_filter(8.0, 2.0, 1.0) = %.2f (esperado: 8.00)\n", low_pass_filter(8.0, 2.0, 1.0));
    return 0;
}
```

---

## EJERCICIO 13: Máquina de Estados de Semáforo
**Contexto**: Implementar lógica de transición de estados

```c
// Estados: 0=Rojo, 1=Amarillo, 2=Verde
// Prototipo de función
int next_traffic_state(int current_state);

// Test case en main()
int main() {
    printf("Test 1: next_traffic_state(0) = %d (esperado: 2)\n", next_traffic_state(0));  // Rojo -> Verde
    printf("Test 2: next_traffic_state(2) = %d (esperado: 1)\n", next_traffic_state(2));  // Verde -> Amarillo
    printf("Test 3: next_traffic_state(1) = %d (esperado: 0)\n", next_traffic_state(1));  // Amarillo -> Rojo
    return 0;
}
```

---

## EJERCICIO 14: Cálculo de Eficiencia de Motor
**Contexto**: Calcular eficiencia porcentual de motor eléctrico

```c
// Prototipo de función
float motor_efficiency(float power_output, float power_input);

// Test case en main()
int main() {
    printf("Test 1: motor_efficiency(750.0, 1000.0) = %.2f (esperado: 75.00)\n", motor_efficiency(750.0, 1000.0));
    printf("Test 2: motor_efficiency(450.0, 500.0) = %.2f (esperado: 90.00)\n", motor_efficiency(450.0, 500.0));
    printf("Test 3: motor_efficiency(0.0, 100.0) = %.2f (esperado: 0.00)\n", motor_efficiency(0.0, 100.0));
    return 0;
}
```

---

## EJERCICIO 15: Búsqueda de Valor Máximo en Sensores
**Contexto**: Encontrar la lectura máxima en array de sensores

```c
// Prototipo de función
float find_max_sensor(float sensors[], int count);

// Test case en main()
int main() {
    float test1[] = {23.5, 28.1, 25.8, 31.2, 22.9};
    float test2[] = {-5.0, -10.0, -2.0, -15.0};
    float test3[] = {100.0};
    
    printf("Test 1: find_max_sensor(test1, 5) = %.2f (esperado: 31.20)\n", find_max_sensor(test1, 5));
    printf("Test 2: find_max_sensor(test2, 4) = %.2f (esperado: -2.00)\n", find_max_sensor(test2, 4));
    printf("Test 3: find_max_sensor(test3, 1) = %.2f (esperado: 100.00)\n", find_max_sensor(test3, 1));
    return 0;
}
```

---

## EJERCICIO 16: Control de Histéresis para Relé
**Contexto**: Implementar control on/off con histéresis para evitar oscilaciones

```c
// Prototipo de función (retorna 1=ON, 0=OFF)
int hysteresis_control(float input, float setpoint, float hysteresis, int previous_state);

// Test case en main()
int main() {
    printf("Test 1: hysteresis_control(22.0, 25.0, 2.0, 0) = %d (esperado: 1)\n", hysteresis_control(22.0, 25.0, 2.0, 0));
    printf("Test 2: hysteresis_control(26.0, 25.0, 2.0, 1) = %d (esperado: 1)\n", hysteresis_control(26.0, 25.0, 2.0, 1));
    printf("Test 3: hysteresis_control(28.0, 25.0, 2.0, 1) = %d (esperado: 0)\n", hysteresis_control(28.0, 25.0, 2.0, 1));
    return 0;
}
```

---

## EJERCICIO 17: Decodificador de Señales Digitales
**Contexto**: Convertir 4 bits en valor decimal para control digital

```c
// Prototipo de función
int decode_4bit(int bit3, int bit2, int bit1, int bit0);

// Test case en main()
int main() {
    printf("Test 1: decode_4bit(1, 0, 1, 0) = %d (esperado: 10)\n", decode_4bit(1, 0, 1, 0));
    printf("Test 2: decode_4bit(1, 1, 1, 1) = %d (esperado: 15)\n", decode_4bit(1, 1, 1, 1));
    printf("Test 3: decode_4bit(0, 0, 0, 1) = %d (esperado: 1)\n", decode_4bit(0, 0, 0, 1));
    return 0;
}
```

---

## EJERCICIO 18: Control PID Simplificado (Solo Proporcional)
**Contexto**: Implementar control proporcional para sistema de posicionamiento

```c
// Prototipo de función
float proportional_control(float setpoint, float current_position, float kp);

// Test case en main()
int main() {
    printf("Test 1: proportional_control(50.0, 40.0, 0.5) = %.2f (esperado: 5.00)\n", proportional_control(50.0, 40.0, 0.5));
    printf("Test 2: proportional_control(25.0, 30.0, 1.2) = %.2f (esperado: -6.00)\n", proportional_control(25.0, 30.0, 1.2));
    printf("Test 3: proportional_control(100.0, 100.0, 2.0) = %.2f (esperado: 0.00)\n", proportional_control(100.0, 100.0, 2.0));
    return 0;
}
```

---

## EJERCICIO 19: Calculadora de Tiempo de Rampa
**Contexto**: Calcular tiempo necesario para acelerar/desacelerar motor

```c
// Prototipo de función
float ramp_time(float initial_speed, float final_speed, float acceleration);

// Test case en main()
int main() {
    printf("Test 1: ramp_time(0.0, 100.0, 10.0) = %.2f (esperado: 10.00)\n", ramp_time(0.0, 100.0, 10.0));
    printf("Test 2: ramp_time(50.0, 20.0, 5.0) = %.2f (esperado: 6.00)\n", ramp_time(50.0, 20.0, 5.0));
    printf("Test 3: ramp_time(25.0, 25.0, 3.0) = %.2f (esperado: 0.00)\n", ramp_time(25.0, 25.0, 3.0));
    return 0;
}
```

---

## EJERCICIO 20: Validador de Secuencia de Encoder
**Contexto**: Verificar que secuencia de encoder sea válida (Gray code)

```c
// Prototipo de función (secuencias válidas: 00->01->11->10->00)
int validate_encoder_sequence(int seq[], int length);

// Test case en main()
int main() {
    int valid1[] = {0, 0, 0, 1, 1, 1, 1, 0};      // 00->01->11->10
    int invalid1[] = {0, 0, 1, 1, 0, 0};           // salto inválido
    int valid2[] = {1, 0, 0, 0, 0, 1};             // 10->00->01
    
    printf("Test 1: validate_encoder_sequence(valid1, 8) = %d (esperado: 1)\n", validate_encoder_sequence(valid1, 8));
    printf("Test 2: validate_encoder_sequence(invalid1, 6) = %d (esperado: 0)\n", validate_encoder_sequence(invalid1, 6));
    printf("Test 3: validate_encoder_sequence(valid2, 6) = %d (esperado: 1)\n", validate_encoder_sequence(valid2, 6));
    return 0;
}
```

---

## EJERCICIO 21: Control de Múltiples Actuadores
**Contexto**: Activar actuadores basado en prioridades y estado del sistema

```c
// Prototipo de función (retorna máscara de bits: bit 0=actuador1, bit 1=actuador2, etc.)
int actuator_control(int priorities[], int states[], int count, int max_active);

// Test case en main()
int main() {
    int prio1[] = {3, 1, 4, 2};    // prioridades (mayor número = mayor prioridad)
    int state1[] = {1, 1, 1, 0};   // estados solicitados (1=activar, 0=desactivar)
    
    int prio2[] = {5, 2, 8, 1};
    int state2[] = {1, 1, 1, 1};
    
    printf("Test 1: actuator_control(prio1, state1, 4, 2) = %d (esperado: 5)\n", actuator_control(prio1, state1, 4, 2));  // bits 0 y 2
    printf("Test 2: actuator_control(prio2, state2, 4, 3) = %d (esperado: 14)\n", actuator_control(prio2, state2, 4, 3)); // bits 1, 2 y 3
    return 0;
}
```

---

## EJERCICIO 22: Interpolación Lineal para Calibración
**Contexto**: Interpolar valores entre puntos de calibración conocidos

```c
// Prototipo de función
float linear_interpolation(float x, float x1, float y1, float x2, float y2);

// Test case en main()
int main() {
    printf("Test 1: linear_interpolation(5.0, 0.0, 0.0, 10.0, 100.0) = %.2f (esperado: 50.00)\n", 
           linear_interpolation(5.0, 0.0, 0.0, 10.0, 100.0));
    printf("Test 2: linear_interpolation(2.5, 2.0, 10.0, 3.0, 20.0) = %.2f (esperado: 15.00)\n", 
           linear_interpolation(2.5, 2.0, 10.0, 3.0, 20.0));
    printf("Test 3: linear_interpolation(7.0, 5.0, 25.0, 5.0, 25.0) = %.2f (esperado: 25.00)\n", 
           linear_interpolation(7.0, 5.0, 25.0, 5.0, 25.0));
    return 0;
}
```

---

## EJERCICIO 23: Detector de Flancos en Señal Digital
**Contexto**: Detectar transiciones positivas en array de señal digital

```c
// Prototipo de función (cuenta flancos de subida 0->1)
int count_rising_edges(int signal[], int length);

// Test case en main()
int main() {
    int test1[] = {0, 1, 1, 0, 1, 0, 1};
    int test2[] = {1, 1, 1, 1};
    int test3[] = {0, 1, 0, 1, 0, 1};
    
    printf("Test 1: count_rising_edges(test1, 7) = %d (esperado: 3)\n", count_rising_edges(test1, 7));
    printf("Test 2: count_rising_edges(test2, 4) = %d (esperado: 0)\n", count_rising_edges(test2, 4));
    printf("Test 3: count_rising_edges(test3, 6) = %d (esperado: 3)\n", count_rising_edges(test3, 6));
    return 0;
}
```

---

## EJERCICIO 24: Control de Ventilador con Temperatura
**Contexto**: Control de velocidad de ventilador basado en curva de temperatura

```c
// Prototipo de función (velocidad 0-100%)
int fan_speed_control(float temperature);

// Test case en main()
int main() {
    printf("Test 1: fan_speed_control(20.0) = %d (esperado: 0)\n", fan_speed_control(20.0));    // temp < 25: off
    printf("Test 2: fan_speed_control(30.0) = %d (esperado: 25)\n", fan_speed_control(30.0));   // temp 25-35: 25%
    printf("Test 3: fan_speed_control(45.0) = %d (esperado: 75)\n", fan_speed_control(45.0));   // temp 35-50: 75%
    printf("Test 4: fan_speed_control(60.0) = %d (esperado: 100)\n", fan_speed_control(60.0));  // temp >50: 100%
    return 0;
}
```

---

## EJERCICIO 25: Calculadora de Resistencia Equivalente
**Contexto**: Calcular resistencia equivalente de resistencias en paralelo

```c
// Prototipo de función (1/Req = 1/R1 + 1/R2 + ... + 1/Rn)
float parallel_resistance(float resistors[], int count);

// Test case en main()
int main() {
    float test1[] = {100.0, 200.0};               // 1/Req = 1/100 + 1/200 = 0.015, Req = 66.67
    float test2[] = {10.0, 10.0, 10.0};           // 1/Req = 0.3, Req = 3.33
    float test3[] = {50.0};                        // Req = 50.0
    
    printf("Test 1: parallel_resistance(test1, 2) = %.2f (esperado: 66.67)\n", parallel_resistance(test1, 2));
    printf("Test 2: parallel_resistance(test2, 3) = %.2f (esperado: 3.33)\n", parallel_resistance(test2, 3));
    printf("Test 3: parallel_resistance(test3, 1) = %.2f (esperado: 50.00)\n", parallel_resistance(test3, 1));
    return 0;
}
```

---

## EJERCICIO 26: Sistema de Alarmas por Prioridad
**Contexto**: Gestionar múltiples alarmas y retornar la de mayor prioridad activa

```c
// Prototipo de función (retorna índice de alarma de mayor prioridad, -1 si no hay)
int highest_priority_alarm(int alarms[], int priorities[], int count);

// Test case en main()
int main() {
    int alarms1[] = {0, 1, 0, 1};        // alarmas activas en posición 1 y 3
    int priorities1[] = {1, 3, 2, 5};    // prioridades correspondientes
    
    int alarms2[] = {0, 0, 0, 0};        // sin alarmas
    int priorities2[] = {1, 2, 3, 4};
    
    int alarms3[] = {1, 1, 1, 0};        // alarmas en 0, 1, 2
    int priorities3[] = {8, 2, 5, 1};
    
    printf("Test 1: highest_priority_alarm(alarms1, priorities1, 4) = %d (esperado: 3)\n", 
           highest_priority_alarm(alarms1, priorities1, 4));
    printf("Test 2: highest_priority_alarm(alarms2, priorities2, 4) = %d (esperado: -1)\n", 
           highest_priority_alarm(alarms2, priorities2, 4));
    printf("Test 3: highest_priority_alarm(alarms3, priorities3, 4) = %d (esperado: 0)\n", 
           highest_priority_alarm(alarms3, priorities3, 4));
    return 0;
}
```

---

## EJERCICIO 27: Control de Posición con Zona Muerta
**Contexto**: Implementar zona muerta en control de posición para evitar oscilaciones

```c
// Prototipo de función (retorna 0 si está en zona muerta, sino retorna error)
float deadband_control(float setpoint, float current_position, float deadband);

// Test case en main()
int main() {
    printf("Test 1: deadband_control(100.0, 99.5, 1.0) = %.2f (esperado: 0.00)\n", deadband_control(100.0, 99.5, 1.0));
    printf("Test 2: deadband_control(50.0, 48.0, 1.5) = %.2f (esperado: 2.00)\n", deadband_control(50.0, 48.0, 1.5));
    printf("Test 3: deadband_control(25.0, 27.0, 1.0) = %.2f (esperado: -2.00)\n", deadband_control(25.0, 27.0, 1.0));
    return 0;
}
```

---

## EJERCICIO 28: Generador de Secuencia de Pasos para Motor
**Contexto**: Generar secuencia de activación para motor paso a paso (4 fases)

```c
// Prototipo de función (llena array con secuencia: [1,0,0,0], [0,1,0,0], [0,0,1,0], [0,0,0,1])
void stepper_sequence(int output[][4], int steps);

// Test case en main()
int main() {
    int sequence1[6][4];
    int sequence2[3][4];
    
    stepper_sequence(sequence1, 6);
    stepper_sequence(sequence2, 3);
    
    printf("Test 1 (6 pasos):\n");
    for(int i = 0; i < 6; i++) {
        printf("Paso %d: [%d,%d,%d,%d]\n", i, sequence1[i][0], sequence1[i][1], sequence1[i][2], sequence1[i][3]);
    }
    
    printf("\nTest 2 (3 pasos):\n");
    for(int i = 0; i < 3; i++) {
        printf("Paso %d: [%d,%d,%d,%d]\n", i, sequence2[i][0], sequence2[i][1], sequence2[i][2], sequence2[i][3]);
    }
    
    return 0;
}
```

---

## EJERCICIO 29: Calculadora de Consumo Energético
**Contexto**: Calcular consumo total de energía de múltiples dispositivos

```c
// Estructura para dispositivo
typedef struct {
    float power_watts;
    float hours_on;
} Device;

// Prototipo de función (retorna kWh total)
float total_energy_consumption(Device devices[], int count);

// Test case en main()
int main() {
    Device test1[] = {{1000.0, 8.0}, {500.0, 12.0}, {200.0, 24.0}};  // Motor, Bomba, Control
    Device test2[] = {{750.0, 4.0}};                                   // Un solo motor
    Device test3[] = {{100.0, 2.0}, {150.0, 6.0}, {300.0, 1.0}};    // Varios pequeños
    
    printf("Test 1: total_energy_consumption(test1, 3) = %.2f (esperado: 18.80 kWh)\n", total_energy_consumption(test1, 3));
    printf("Test 2: total_energy_consumption(test2, 1) = %.2f (esperado: 3.00 kWh)\n", total_energy_consumption(test2, 1));
    printf("Test 3: total_energy_consumption(test3, 3) = %.2f (esperado: 1.40 kWh)\n", total_energy_consumption(test3, 3));
    return 0;
}
```

---

## EJERCICIO 30: Control de Acceso Multi-Condición
**Contexto**: Sistema de acceso que evalúa múltiples sensores de seguridad

```c
// Prototipo de función (1=acceso permitido, 0=denegado)
int access_control(int card_valid, int fingerprint_ok, int door_closed, int emergency_stop);

// Test case en main()
int main() {
    printf("Test 1: access_control(1, 1, 1, 0) = %d (esperado: 1)\n", access_control(1, 1, 1, 0));  // Todo OK
    printf("Test 2: access_control(1, 0, 1, 0) = %d (esperado: 0)\n", access_control(1, 0, 1, 0));  // Sin huella
    printf("Test 3: access_control(1, 1, 0, 0) = %d (esperado: 0)\n", access_control(1, 1, 0, 1));  // Emergencia
    printf("Test 4: access_control(0, 1, 1, 0) = %d (esperado: 0)\n", access_control(0, 1, 1, 0));  // Sin tarjeta
    return 0;
}
```

---

## EJERCICIO 31: Filtro de Mediana para Ruido Impulsivo
**Contexto**: Implementar filtro de mediana para eliminar picos en sensores

```c
// Prototipo de función (encuentra mediana de 3 valores consecutivos)
void median_filter(float input[], float output[], int length);

// Test case en main()
int main() {
    float input1[] = {1.0, 10.0, 2.0, 3.0, 15.0, 4.0, 5.0};  // con picos en pos 1 y 4
    float output1[7];
    float input2[] = {5.0, 5.1, 4.9, 5.0};
    float output2[4];
    
    median_filter(input1, output1, 7);
    median_filter(input2, output2, 4);
    
    printf("Test 1 - Filtrado con picos:\n");
    printf("Input : "); for(int i=0; i<7; i++) printf("%.1f ", input1[i]); printf("\n");
    printf("Output: "); for(int i=0; i<7; i++) printf("%.1f ", output1[i]); printf("\n");
    
    printf("\nTest 2 - Señal estable:\n");
    printf("Input : "); for(int i=0; i<4; i++) printf("%.1f ", input2[i]); printf("\n");
    printf("Output: "); for(int i=0; i<4; i++) printf("%.1f ", output2[i]); printf("\n");
    
    return 0;
}
```

---

## EJERCICIO 32: Controlador de Múltiples Zonas de Temperatura
**Contexto**: Controlar calefacción/refrigeración en múltiples zonas independientes

```c
// Prototipo de función (llena array de salidas: -1=enfriar, 0=off, 1=calentar)
void multi_zone_control(float temperatures[], float setpoints[], int outputs[], int zones);

// Test case en main()
int main() {
    float temps1[] = {18.5, 23.2, 26.8, 19.1};
    float setpoints1[] = {22.0, 24.0, 25.0, 20.0};
    int outputs1[4];
    
    float temps2[] = {22.0, 22.0};
    float setpoints2[] = {22.0, 22.0};
    int outputs2[2];
    
    multi_zone_control(temps1, setpoints1, outputs1, 4);
    multi_zone_control(temps2, setpoints2, outputs2, 2);
    
    printf("Test 1:\n");
    for(int i = 0; i < 4; i++) {
        printf("Zona %d: %.1f°C -> Setpoint %.1f°C = Acción %d\n", 
               i, temps1[i], setpoints1[i], outputs1[i]);
    }
    
    printf("\nTest 2:\n");
    for(int i = 0; i < 2; i++) {
        printf("Zona %d: %.1f°C -> Setpoint %.1f°C = Acción %d\n", 
               i, temps2[i], setpoints2[i], outputs2[i]);
    }
    
    return 0;
}
```

---

## EJERCICIO 33: Analizador de Frecuencia de Pulsos
**Contexto**: Calcular frecuencia de señal basada en tiempo entre pulsos

```c
// Prototipo de función (array con tiempos en ms entre flancos ascendentes)
float calculate_frequency(int pulse_times[], int count);

// Test case en main()
int main() {
    int times1[] = {100, 100, 100, 100};  // 100ms entre pulsos = 10Hz
    int times2[] = {50, 50, 50};          // 50ms entre pulsos = 20Hz  
    int times3[] = {200, 200};            // 200ms entre pulsos = 5Hz
    
    printf("Test 1: calculate_frequency(times1, 4) = %.2f (esperado: 10.00 Hz)\n", calculate_frequency(times1, 4));
    printf("Test 2: calculate_frequency(times2, 3) = %.2f (esperado: 20.00 Hz)\n", calculate_frequency(times2, 3));
    printf("Test 3: calculate_frequency(times3, 2) = %.2f (esperado: 5.00 Hz)\n", calculate_frequency(times3, 2));
    return 0;
}
```

---

## EJERCICIO 34: Optimizador de Trayectoria 2D
**Contexto**: Encontrar el punto más cercano en una trayectoria dada

```c
// Estructura para punto 2D
typedef struct {
    float x, y;
} Point2D;

// Prototipo de función (retorna índice del punto más cercano)
int find_closest_point(Point2D target, Point2D trajectory[], int count);

// Test case en main()
int main() {
    Point2D target1 = {5.0, 5.0};
    Point2D path1[] = {{0,0}, {3,4}, {6,2}, {8,8}, {2,7}};
    
    Point2D target2 = {1.0, 1.0};
    Point2D path2[] = {{0,0}, {10,10}, {-5,-5}};
    
    printf("Test 1: find_closest_point({5,5}, path1, 5) = %d (esperado: 2)\n", 
           find_closest_point(target1, path1, 5));
    printf("Test 2: find_closest_point({1,1}, path2, 3) = %d (esperado: 0)\n", 
           find_closest_point(target2, path2, 3));
           
    return 0;
}
```

---

## EJERCICIO 35: Sistema de Backup Automático
**Contexto**: Seleccionar sistema de backup basado en fallas detectadas

```c
// Prototipo de función (retorna sistema a usar: 0=principal, 1=backup1, 2=backup2, -1=falla total)
int backup_selector(int main_system, int backup1, int backup2);

// Test case en main()
int main() {
    printf("Test 1: backup_selector(1, 1, 1) = %d (esperado: 0)\n", backup_selector(1, 1, 1));    // Todo OK
    printf("Test 2: backup_selector(0, 1, 1) = %d (esperado: 1)\n", backup_selector(0, 1, 1));    // Principal falla
    printf("Test 3: backup_selector(0, 0, 1) = %d (esperado: 2)\n", backup_selector(0, 0, 1));    // Solo backup2
    printf("Test 4: backup_selector(0, 0, 0) = %d (esperado: -1)\n", backup_selector(0, 0, 0));   // Todo falla
    return 0;
}
```

---

## EJERCICIO 36: Calculadora de Inercia Rotacional
**Contexto**: Calcular momento de inercia de sistema con múltiples masas

```c
// Estructura para masa puntual
typedef struct {
    float mass;      // kg
    float radius;    // m desde eje de rotación
} PointMass;

// Prototipo de función (I = Σ(m * r²))
float rotational_inertia(PointMass masses[], int count);

// Test case en main()
int main() {
    PointMass system1[] = {{2.0, 1.0}, {3.0, 2.0}, {1.0, 0.5}};     // I = 2*1 + 3*4 + 1*0.25 = 14.25
    PointMass system2[] = {{5.0, 0.0}};                               // I = 0 (en el eje)
    PointMass system3[] = {{1.0, 1.0}, {1.0, 1.0}};                 // I = 1 + 1 = 2
    
    printf("Test 1: rotational_inertia(system1, 3) = %.2f (esperado: 14.25)\n", rotational_inertia(system1, 3));
    printf("Test 2: rotational_inertia(system2, 1) = %.2f (esperado: 0.00)\n", rotational_inertia(system2, 1));
    printf("Test 3: rotational_inertia(system3, 2) = %.2f (esperado: 2.00)\n", rotational_inertia(system3, 2));
    return 0;
}
```

---

## EJERCICIO 37: Monitor de Vibración con FFT Básica
**Contexto**: Detectar frecuencia dominante en señal de vibración (versión simplificada)

```c
// Prototipo de función (encuentra frecuencia con mayor amplitud)
float dominant_frequency(float amplitudes[], float frequencies[], int count);

// Test case en main()
int main() {
    float amps1[] = {0.1, 0.8, 0.3, 0.2};
    float freqs1[] = {10.0, 60.0, 120.0, 180.0};
    
    float amps2[] = {0.5, 0.2, 0.9, 0.1};
    float freqs2[] = {25.0, 50.0, 75.0, 100.0};
    
    printf("Test 1: dominant_frequency(amps1, freqs1, 4) = %.1f (esperado: 60.0 Hz)\n", 
           dominant_frequency(amps1, freqs1, 4));
    printf("Test 2: dominant_frequency(amps2, freqs2, 4) = %.1f (esperado: 75.0 Hz)\n", 
           dominant_frequency(amps2, freqs2, 4));
    return 0;
}
```

---

## EJERCICIO 38: Control de Flujo con Válvulas Proporcionales
**Contexto**: Controlar flujo mediante válvulas con respuesta no-lineal

```c
// Prototipo de función (convierte % flujo deseado a % apertura de válvula)
// Relación: flujo = sqrt(apertura * 100)
float flow_to_valve_opening(float desired_flow_percent);

// Test case en main()
int main() {
    printf("Test 1: flow_to_valve_opening(50.0) = %.2f (esperado: 25.00)\n", flow_to_valve_opening(50.0));   // 50 = sqrt(25*100)
    printf("Test 2: flow_to_valve_opening(70.71) = %.2f (esperado: 50.00)\n", flow_to_valve_opening(70.71)); // 70.71 = sqrt(50*100)
    printf("Test 3: flow_to_valve_opening(100.0) = %.2f (esperado: 100.00)\n", flow_to_valve_opening(100.0)); // 100 = sqrt(100*100)
    return 0;
}
```

---

## EJERCICIO 39: Planificador de Tareas en Tiempo Real
**Contexto**: Determinar qué tarea ejecutar basado en prioridades y tiempos

```c
// Estructura para tarea
typedef struct {
    int id;
    int priority;        // mayor número = mayor prioridad
    int time_since_run;  // ms desde última ejecución
    int period;          // ms entre ejecuciones requeridas
} Task;

// Prototipo de función (retorna ID de tarea a ejecutar, -1 si ninguna)
int schedule_next_task(Task tasks[], int count);

// Test case en main()
int main() {
    Task tasks1[] = {
        {1, 5, 50, 100},   // alta prioridad, debe ejecutar en 50ms más
        {2, 3, 80, 200},   // media prioridad, debe ejecutar en 120ms más  
        {3, 1, 150, 100}   // baja prioridad, ya pasó 50ms del período
    };
    
    Task tasks2[] = {
        {1, 2, 10, 100},   // no urgente
        {2, 1, 20, 200}    // no urgente
    };
    
    printf("Test 1: schedule_next_task(tasks1, 3) = %d (esperado: 3)\n", schedule_next_task(tasks1, 3));
    printf("Test 2: schedule_next_task(tasks2, 2) = %d (esperado: -1)\n", schedule_next_task(tasks2, 2));
    return 0;
}
```

---

## EJERCICIO 40: Sistema de Monitoreo Predictivo
**Contexto**: Predecir falla basada en tendencia de múltiples parámetros

```c
// Prototipo de función (analiza tendencia: -1=mejorando, 0=estable, 1=deteriorando, 2=falla crítica)
int predictive_maintenance(float current[], float previous[], float thresholds[], int param_count);

// Test case en main()
int main() {
    float current1[] = {75.0, 2.1, 45.0};      // temp, vibración, ruido
    float previous1[] = {70.0, 1.8, 40.0};     // valores anteriores
    float thresholds1[] = {80.0, 3.0, 50.0};   // límites críticos
    
    float current2[] = {85.0, 3.5, 55.0};      // valores críticos
    float previous2[] = {82.0, 3.2, 52.0};     
    float thresholds2[] = {80.0, 3.0, 50.0};
    
    float current3[] = {65.0, 1.5, 35.0};      // mejorando
    float previous3[] = {70.0, 2.0, 40.0};     
    float thresholds3[] = {80.0, 3.0, 50.0};
    
    printf("Test 1: predictive_maintenance(current1, previous1, thresholds1, 3) = %d (esperado: 1)\n", 
           predictive_maintenance(current1, previous1, thresholds1, 3));
    printf("Test 2: predictive_maintenance(current2, previous2, thresholds2, 3) = %d (esperado: 2)\n", 
           predictive_maintenance(current2, previous2, thresholds2, 3));
    printf("Test 3: predictive_maintenance(current3, previous3, thresholds3, 3) = %d (esperado: -1)\n", 
           predictive_maintenance(current3, previous3, thresholds3, 3));
    return 0;
}
```

---

## ESTRUCTURA DEL REPOSITORIO SUGERIDA

```
ejercicios-c-mecatronica/
├── README.md
├── ejercicio_01/
│   ├── main.c              (con test cases)
│   ├── solucion.c          (archivo para estudiante)
│   └── README.md           (instrucciones específicas)
├── ejercicio_02/
│   └── ...
├── ejercicio_40/
│   └── ...
├── plantillas/
│   ├── template.c          (estructura base)
│   └── Makefile
├── recursos/
│   ├── funciones_math.h    (funciones matemáticas permitidas)
│   └── constantes.h        (constantes físicas)
└── evaluacion/
    ├── script_test.sh      (script de evaluación automática)
    └── rubricas.md         (criterios de calificación)
```

---

## CRITERIOS DE EVALUACIÓN

### Por Ejercicio (100 puntos total):
- **Funcionamiento (60 pts)**: Pasa todos los test cases
- **Estilo de código (20 pts)**: Indentación, nombres de variables, comentarios
- **Eficiencia (10 pts)**: Algoritmo apropiado para el problema
- **Validación de entrada (10 pts)**: Manejo de casos extremos

### Distribución Temporal Sugerida:
- **Día 1-2**: Ejercicios 1-10 (Básicos)
- **Día 3-4**: Ejercicios 11-20 (Variables y decisiones)
- **Día 5-6**: Ejercicios 21-30 (Ciclos y arreglos)
- **Día 7**: Ejercicios 31-40 (Funciones avanzadas y sistemas complejos)

**Total: 40 ejercicios** que cubren progresivamente todos los conceptos con enfoque en mecatrónica.