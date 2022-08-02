## Excelente tutorial sobre auto alinhamento do Eixo Z
[All Things Z - Deep Dive - Marlin Tricks - Chris's Basement](https://www.youtube.com/watch?v=3jAFQdTk8iw)



Z_MIN_PROBE_PIN 32

Z_MIN_PROBE_ENDSTOP_INVERTING

Z_PROBE_SERVO_NR 0   
Z_SERVO_ANGLES { 46, 1 } 



 
      +-- BACK ---+
      |    [+]    |
    L |        1  | R <-- Example "1" (right+,  back+)
    E |  2        | I <-- Example "2" ( left-,  back+)
    F |[-]  N  [+]| G <-- Nozzle
    T |       3   | H <-- Example "3" (right+, front-)
      | 4         | T <-- Example "4" ( left-, front-)
      |    [-]    |
      O-- FRONT --+
 
 
NOZZLE_TO_PROBE_OFFSET { 42, 7, 0 }

Most probes should stay away from the edges of the bed, but
with NOZZLE_AS_PROBE this can be negative for a wider probing area.
PROBING_MARGIN 42

X and Y axis travel speed (mm/min) between probes
XY_PROBE_FEEDRATE (133*60)

Feedrate (mm/min) for the first approach when double-probing (MULTIPLE_PROBING == 2)
Z_PROBE_FEEDRATE_FAST (4*60)

Feedrate (mm/min) for the "accurate" probe of each point
Z_PROBE_FEEDRATE_SLOW (Z_PROBE_FEEDRATE_FAST / 2)

MULTIPLE_PROBING 2

AUTO_BED_LEVELING_BILINEAR

RESTORE_LEVELING_AFTER_G28

Testar essa configuração
PREHEAT_BEFORE_LEVELING

Ligar essa
DEBUG_LEVELING_FEATURE

Testar
ENABLE_LEVELING_FADE_HEIGHT

Conferir
Z_SAFE_HOMING

Ajustar. Parece estar muito rápido
HOMING_FEEDRATE_MM_M { (100*60), (100*60), (4*60) }

