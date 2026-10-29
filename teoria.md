# Teoría · Pieza NN: Nombre de la pieza

**Grupo:** Marco Ariza · Antonio Montero **
# Hoja de teoría: Fuente de alimentación (PSU)

## 1. Concepto y función

La **fuente de alimentación** convierte la **corriente alterna (AC)** de la red (230 V, 50 Hz en España) en **corriente continua (DC)** de bajo voltaje: **+12 V, +5 V, +3,3 V**, además de −12 V y +5VSB.
Funciones: **rectificar, transformar, estabilizar y proteger**.

## 2. Funcionamiento (fuente conmutada, SMPS)

**Filtro EMI → rectificador + condensador → PFC activo → troceador + transformador de alta frecuencia → rectificación + filtro → salidas DC**, con **control PWM** que realimenta y estabiliza.

- Trabaja a **alta frecuencia** (decenas de kHz): componentes pequeños y eficientes.
- El **transformador** reduce el voltaje y **aísla** la salida de la red.
- **PFC activo:** mejora el factor de potencia.

## 3. Raíles y tensiones

| Raíl | Alimenta principalmente | Color del cable |
|---|---|---|
| **+12 V** | CPU, GPU, ventiladores, discos (motor) | Amarillo |
| **+5 V** | SSD/HDD (lógica), USB | Rojo |
| **+3,3 V** | Memoria, lógica de la placa | Naranja |
| **+5VSB** | Placa base en espera (standby) | Morado |
| **−12 V** | Antiguos puertos serie (casi sin uso) | Azul |
| Masa (GND) | Retorno | Negro |

Tolerancia ATX: **±5 %** en +12 V, +5 V y +3,3 V.

## 4. Magnitudes y unidades

| Magnitud | Unidad | Fórmula / idea |
|---|---|---|
| Potencia | **W** | P = V · I |
| Tensión | **V** | Nivel de cada raíl |
| Corriente | **A** | Máxima por raíl |
| Eficiencia | **%** | η = P_salida / P_entrada · 100 |
| Rizado | **mV** | Ondulación residual en DC |
| Ruido | **dB(A)** | Sonómetro |

Ejemplo: 62,5 A × 12 V = **750 W**. Con η = 90 % y 500 W de salida, la entrada es 500 / 0,9 ≈ **556 W**.

## 5. Tipos

- **Formato:** **ATX** (sobremesa), **SFX / SFX-L** (cajas pequeñas), **TFX**, **Flex ATX**.
- **Cableado:** **no modular** · **semimodular** · **totalmente modular**.
- **Raíles +12 V:** **único** (toda la corriente en un raíl) o **múltiple** (varios con protección propia).

## 6. Estándares y evolución

| Estándar | Novedad clave |
|---|---|
| **AT** | Interruptor mecánico |
| **ATX (1995)** | Apagado por software, +5VSB |
| **ATX12V** | Conector de 4 pines CPU y 24 pines placa |
| **ATX 3.0 (2022)** | Conector **12VHPWR** (hasta 600 W), tolerancia a picos |
| **ATX 3.1 (2024)** | Conector **12V-2x6**, requisitos más estrictos |

## 7. Eficiencia: certificación 80 PLUS (115 V)

| Nivel | 20 % | 50 % | 100 % |
|---|---|---|---|
| 80 PLUS | 80 | 80 | 80 |
| Bronze | 82 | 85 | 82 |
| Silver | 85 | 88 | 85 |
| **Gold** | **87** | **90** | **87** |
| Platinum | 90 | 92 | 89 |
| Titanium | 92 | 94 | 90 |

Orden de menor a mayor: **Estándar < Bronze < Silver < Gold < Platinum < Titanium**.
Cybenetics es otra certificación (eficiencia **y** ruido).

## 8. Datos clave

- Una fuente **sobredimensionada un 20–30 %** trabaja más fresca y con mejor eficiencia.
- Potencia **continua** ≠ potencia **pico**.
- **No mezclar cables** de fuentes modulares distintas, aunque encajen.
- Averías típicas: **condensadores hinchados**, ventilador bloqueado, fusible quemado, apagados bajo carga.
- Dentro de la fuente hay **tensión peligrosa** aunque esté desenchufada.

---

## Preguntas tipo test

**1. ¿Cuál es la función principal de una fuente de alimentación de PC?**
- a) Almacenar energía para cortes de luz
- b) Convertir AC de la red en DC de bajo voltaje para los componentes ✅
- c) Aumentar la tensión de la red
- d) Refrigerar la placa base

*Explicación: rectifica, transforma y estabiliza la corriente que necesitan CPU, placa, GPU y discos.*

**2. ¿Qué raíl suministra la mayor parte de la potencia en una fuente ATX moderna?**
- a) +3,3 V
- b) +5 V
- c) +12 V ✅
- d) −12 V

*Explicación: CPU y GPU se alimentan de +12 V, por eso concentra casi toda la potencia.*

**3. ¿Qué función tiene la etapa PFC activa?**
- a) Refrigerar el transformador
- b) Mejorar el factor de potencia ✅
- c) Convertir DC en AC
- d) Detectar cortocircuitos en la salida

*Explicación: el PFC hace que la corriente de entrada esté en fase con la tensión.*

**4. Una fuente entrega 500 W y consume 556 W de la red. ¿Cuál es su eficiencia aproximada?**
- a) 80 %
- b) 85 %
- c) 90 % ✅
- d) 95 %

*Explicación: η = 500 / 556 · 100 ≈ 90 %.*

**5. ¿Qué cable (color) corresponde habitualmente a +5VSB?**
- a) Amarillo
- b) Morado ✅
- c) Azul
- d) Naranja

*Explicación: +5VSB (standby) es morado; amarillo es +12 V y naranja +3,3 V.*

**6. ¿Qué estándar introdujo el conector 12VHPWR para GPU?**
- a) ATX 2.0
- b) ATX12V 2.4
- c) ATX 3.0 ✅
- d) AT

*Explicación: ATX 3.0 (2022) lo introdujo; ATX 3.1 lo sustituyó por el 12V-2x6.*

**7. ¿Cuál es el orden correcto de certificaciones 80 PLUS de menor a mayor eficiencia?**
- a) Gold, Silver, Bronze, Platinum
- b) Bronze, Silver, Gold, Platinum ✅
- c) Silver, Bronze, Platinum, Gold
- d) Platinum, Gold, Silver, Bronze

*Explicación: Estándar < Bronze < Silver < Gold < Platinum < Titanium.*

**8. ¿Qué error es más peligroso al instalar una fuente modular?**
- a) Dejar un cable sin usar
- b) Usar cables de otra fuente modular, aunque encajen ✅
- c) Usar menos conectores de los disponibles
- d) Montarla con el ventilador hacia abajo

*Explicación: la asignación de pines puede variar entre modelos y fabricantes y dañar componentes.*
