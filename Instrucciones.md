# Instrucciones de Uso — Medidor de velocidad

## Objetivo
Contar vueltas/tiempos, mostrar **velocidad promedio** o **tiempo total**, correr **LEDs**, y **reiniciar** seguro.

## Flujo
1) `START` → `iniciar_timer()`  
2) Si **pasó el auto**:  
   - Si **faltan vueltas** → `registrar_tiempo(); cantidad_vueltas++`  
   - Si **se completaron** → `mostrar_velocidad()`  
3) Si **botón velocidad** → `mostrar_velocidad()`  
4) Si **botón tiempo total** → `mostrar_tiempo_total()`  
5) LEDs → `prender_LED1()` → `prender_LED2()` → `prender_LED3()` → `prender_LED4()`  
6) Si **botón reinicio** → `reiniciar_display()` → `reiniciar_timer()` → volver al inicio


## Para realizar pruebas
- Un pulso suma 1 vuelta, registra el tiempo y lo va mostrando en el display.  
- Al llegar a `total_vueltas` se muestra la **velocidad promedio** en el display.  
- El pulsador SW1 muestra la velocidad promedio en el display.
- El pulsador SW2 muestra el tiempo total.
- El pulsador SW3 limpia display, resetea el timer y se reinicia el proceso.
